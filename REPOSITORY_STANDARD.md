# Repository Standard

This file is the canonical governance standard for this repository.

It applies to human contributors, AI-assisted contributors, automation, and maintainers.

The repository must remain understandable without AI and usable with AI.

Important repository actions should leave enough evidence for another person to understand what happened, why it happened, what was checked, and what entered `main`.

AI output is not evidence by itself. Git history, diffs, tests, CI results, review records, and human decisions are evidence.

## 1. Source of truth

One rule must have one authoritative home.

Do not maintain the same rule independently in several files.

Other files may reference this standard, but they must not silently redefine it.

If two repository instructions conflict, treat the conflict as a repository defect and resolve it explicitly.

## 2. File creation

Do not create a new file only because it seems useful.

Before creating a file, answer:

- Purpose: what exact job does the file perform?
- Existing source: does another file already perform this job?
- User: is it primarily for a human, AI, GitHub, CI, or the application?
- Type: is it documentation, a rule, a prompt, configuration, source code, a test, data, or evidence?
- Location: why does it belong at this path?
- Lifecycle: when should it be changed or removed?

If an existing file already owns the responsibility, modify the existing file instead of creating a competing file.

## 3. Folder creation

A folder must represent a real boundary, not decoration.

Create a folder only when all of these are true:

1. it represents one clear responsibility or domain;
2. multiple related artifacts need that boundary;
3. the parent would otherwise mix unrelated responsibilities;
4. no existing folder correctly owns the content;
5. its purpose can be explained in one simple sentence.

Do not create placeholder folders for future work.

A new top-level folder must be justified in its Pull Request.

## 4. Folder README files

A folder does not automatically require a `README.md`.

Create a folder README only when a person entering the folder would reasonably need additional explanation about why the folder exists, what belongs there, what does not belong there, or what rules apply.

Folder README files must be human-first and AI-readable.

Do not create a README that merely repeats the directory name.

## 5. Naming

Names must describe responsibility rather than fashion, temporary status, or implementation history.

Prefer specific names such as:

- `source-validation`
- `curriculum`
- `evidence`
- `weekly-intelligence`

Avoid vague names such as:

- `stuff`
- `misc`
- `temp`
- `new`
- `final`
- `latest`
- `v2`
- `other`

Do not make AI part of permanent project naming unless AI itself is the real subject of that artifact.

## 6. Trusted branch

`main` is the trusted integration branch.

Normal work must happen outside `main` and enter through a Pull Request.

Do not bypass required review or checks with a direct push to `main`.

## 7. Branch naming

Use this format:

`<type>/<task-id>-<purpose>`

Allowed types:

- `feat`
- `fix`
- `refactor`
- `docs`
- `test`
- `chore`

Examples:

- `docs/001-repository-standard`
- `feat/014-weekly-ingestion`
- `fix/021-source-validation`
- `test/027-curriculum-validator`

Do not use AI authorship as the branch type. Record AI involvement in the Pull Request instead.

## 8. Commit message standard

Use this exact format:

`<type>(scope): <what changed>`

Allowed types only:

- `feat`
- `fix`
- `refactor`
- `docs`
- `test`
- `chore`

Constraints:

- scope must be one word representing the relevant feature or module;
- summary must be specific;
- summary must use present tense;
- the full commit subject must be 72 characters or fewer;
- do not use vague wording such as `update`, `change`, `improve`, `changes`, `stuff`, `misc`, or `work` as a substitute for a specific description.

Examples:

- `docs(governance): define canonical repository standards`
- `feat(ingestion): parse weekly intelligence sources`
- `fix(validation): reject sources without publication dates`
- `test(curriculum): cover duplicate chapter detection`

## 9. Pull Requests

A Pull Request is the review boundary between proposed work and trusted repository state.

Use this PR title format:

`<type>(scope): <what the PR does>`

The same allowed types apply as for commits.

A Pull Request must explain at minimum:

- What: what was done?
- Why: why was it needed?
- Scope: which files or responsibilities were affected?
- Not changed: what important areas were intentionally untouched?
- Verification: what was actually checked?
- Result: what passed, failed, or was not run?
- AI involvement: was AI involved and how?
- Limits: what remains unknown or unfinished?
- Human decision: what does the reviewer need to decide?

A Pull Request must be understandable without access to the original AI or human conversation.

## 10. Human and AI contribution standard

Humans and AI-assisted contributors follow the same structural quality rules.

Human-written work does not bypass naming, commit, test, CI, PR, evidence, or review requirements.

AI receives no special trust.

AI may inspect, propose, write, refactor, test, document, prepare branches, prepare commits, and prepare Pull Requests.

AI must not claim `tested`, `verified`, `passed`, `working`, or `complete` unless corresponding evidence actually exists.

When relevant, AI should distinguish between:

- observed;
- inferred;
- not verified.

AI must read repository-local rules before modifying repository content.

Important project decisions must not exist only in chat history.

## 11. CI enforcement

A rule should be enforced automatically when deterministic enforcement is practical.

Examples include:

- commit format;
- PR title format;
- schema validity;
- tests;
- formatting;
- broken links;
- duplicate identifiers;
- required files.

CI must not pretend to decide subjective meaning that requires human judgment.

CI provides automatic evidence. It does not replace human review.

## 12. Evidence

Evidence must be proportional to the work.

Do not generate extra evidence files for every small change when Git history, diffs, PRs, tests, CI results, and reviews already preserve sufficient evidence.

Create additional evidence artifacts only when the evidence must survive independently or contains information that normal Git and GitHub history does not adequately preserve, such as experiment results, benchmark results, source-analysis records, curriculum decisions, or reproducibility records.

## 13. Reusable prompts and harnesses

Do not create a reusable prompt merely because AI can use one.

Create one only when:

1. the operation will occur repeatedly;
2. consistent AI behavior matters;
3. normal documentation is insufficient;
4. the prompt has clearly defined inputs;
5. the prompt has clearly defined outputs;
6. the result can be verified.

A reusable prompt must reference repository rules instead of redefining them.

## 14. Deletion and deprecation

Delete files or folders when their responsibility no longer exists, they duplicate another authoritative source, a temporary migration is complete, or obsolete configuration has no consumers.

Deprecate instead of immediately deleting when contributors, automation, documentation, or compatibility may still depend on the artifact.

A deprecation should explain:

- why it is deprecated;
- its replacement;
- the migration path;
- the removal condition or date when known.

Git history preserves deleted content. Do not keep dead files only for history.

## 15. Structural change gate

Any contribution introducing a new top-level folder, new governance file, new reusable harness, new CI workflow, new permanent configuration system, or new architectural boundary must explain:

- Purpose: why is it necessary?
- Existing source: why cannot an existing artifact handle it?
- Boundary: what belongs there?
- Exclusions: what must not belong there?
- Authority: is it authoritative or does it reference another source?
- Maintenance: what causes it to change?
- Removal: when would it no longer be needed?

Do not create repository architecture merely because it appears cleaner.

## 16. Exceptions

Repository rules must not be silently bypassed.

If a contribution genuinely cannot comply, the Pull Request must identify:

- Rule: which rule cannot be followed?
- Reason: why?
- Impact: what does the exception affect?
- Duration: temporary or permanent?
- Approval: who approved it?

An exception does not automatically become a new standard.

## 17. Rule precedence

Use this order of authority:

1. `REPOSITORY_STANDARD.md`
2. domain-specific repository rules that explicitly reference this standard;
3. approved task requirements;
4. reusable AI harnesses or prompts;
5. individual AI or human instructions.

A lower level must not silently override a higher level.

## 18. No-compromise invariant

A capable developer who did not participate in the original conversation should be able to inspect the repository and understand what exists, why it exists, what changed, how it was checked, and what remains uncertain.

An AI joining with no conversation memory should be able to discover the same applicable rules from the repository without inventing missing standards.

These two tests guide repository structure and contribution decisions.
