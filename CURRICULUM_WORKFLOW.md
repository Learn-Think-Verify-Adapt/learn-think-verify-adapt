# Curriculum Workflow

This file defines the human-controlled workflow for converting approved Weekly Intelligence into curriculum structure and, only after approval, day-specific learning content.

It is a domain-specific operating rule under `REPOSITORY_STANDARD.md`. If this file conflicts with the repository standard, the repository standard takes precedence.

## 1. Purpose

We use ChatGPT as the working conversation interface. Each week, a human provides the completed Weekly Intelligence. ChatGPT must inspect the current repository standards and existing curriculum before proposing curriculum changes.

The workflow separates curriculum decisions from content writing. A Weekly Intelligence item must not automatically become learning content simply because it is new or interesting.

## 2. Curriculum hierarchy

The curriculum uses this hierarchy:

`Learning Path -> Module -> Chapter`

A Learning Path represents a durable human capability area. A Module develops a meaningful capability or stage within that Learning Path. A Chapter develops one focused idea or capability within the Module.

Technology may provide context, evidence, or examples, but the curriculum should remain centred on durable human capability and the four pillars: Learn, Think, Verify, and Adapt.

## 3. Weekly operating flow

The required sequence is:

`Weekly Intelligence -> repository inspection -> curriculum comparison -> Learning Path / Module / Chapter proposal -> human review -> day-specific content -> human review -> append approved content -> final weekly text file`

Human approval is required at both the curriculum-structure stage and the day-specific content stage. ChatGPT must stop at each gate instead of silently continuing.

## 4. Stage A - Weekly Intelligence input

The human pastes or supplies the completed Weekly Intelligence in ChatGPT.

Before proposing curriculum, ChatGPT must read the current applicable repository standards and inspect the existing curriculum available in the repository. Chat memory or an earlier AI summary must not be treated as the only source of truth.

## 5. Stage B - Curriculum proposal only

ChatGPT analyses the Weekly Intelligence, identifies its durable human meaning, compares it with the existing curriculum, and proposes only the curriculum structure needed for human review.

At this stage the output is limited to:

- Learning Path name;
- Module name;
- Chapter names.

Do not generate morning content, evening content, exercises, explanations, or the weekly text file at this stage.

## 6. Curriculum quality checks

Before presenting a proposal, check:

- Durability: does it develop a lasting human capability rather than merely describe this week's technology or news?
- Hierarchy: do the Chapters belong to the Module, and does the Module belong to the Learning Path?
- Progression: do the Chapters build naturally rather than repeat one another?
- Human meaning: is the capability people should strengthen clear?
- Grounding: can the proposal be traced back to the Weekly Intelligence?
- Existing curriculum: does the proposal avoid unnecessary duplication?
- Pillars: does it meaningfully support Learn, Think, Verify, or Adapt?

Do not manufacture a new Learning Path, Module, or fixed number of Chapters when the Weekly Intelligence does not justify them.

## 7. Gate A - Human curriculum approval

After presenting the Learning Path, Module, and Chapter names, stop.

The human may approve, reject, or request changes. No day-specific learning content may be generated until the curriculum structure is approved.

Once approved, the Learning Path, Module, and Chapter names become the working structure for that weekly authoring cycle unless the human explicitly reopens the decision.

## 8. Stage C - Generate one day at a time

After curriculum approval, generate only the requested day's content. Start with Monday Morning and Monday Evening unless the human explicitly requests another approved day.

Do not generate Tuesday or later days automatically. Each day has its own human review gate.

Monday through Friday normally map to the approved Chapter progression. Saturday is a review and integration day rather than an additional ordinary Chapter.

## 9. Morning content structure

For Monday through Friday, morning content uses this order:

`🌅 <DAY> MORNING`

`*Learning Path <number> – <name>*`

`*Module <number> – <name>*`

`*Chapter <number> – <name>*`

`*Understanding*`

`*Practice*`

`*Looking Ahead*`

`*Learn • Think • Verify • Adapt*`

The content itself must follow `communication-style.md`.

## 10. Evening content structure

For Monday through Friday, evening content uses this order:

`🌙 <DAY> EVENING`

`*Learning Path <number> – <name>*`

`*Module <number> – <name>*`

`*Chapter <number> – <name>*`

`*Looking Back*`

`*Thinking Together*`

`*Moving Forward*`

`*Learn • Think • Verify • Adapt*`

Evening content must add reflection and meaning rather than simply repeat the morning message.

## 11. Saturday review structure

Saturday is the weekly or module review and self-assessment stage. It must not be presented as an ordinary additional Chapter merely to maintain a daily sequence.

Saturday Morning normally uses:

- `*Module Review & Self-Assessment*`
- `*Looking Back*`
- `*Three Key Ideas*`
- `*Self-Assessment*`
- `*Looking Ahead*`

Saturday Evening normally uses:

- `*Module Review & Self-Assessment*`
- `*Looking Back*`
- `*Thinking Together*`
- `*Moving Forward*`

The exact curriculum context must remain consistent with the approved week.

## 12. WhatsApp-ready text format

The approved weekly artifact is plain text intended to remain easy to paste into WhatsApp.

Formatting is part of the content contract. Preserve:

- the `🌅` morning and `🌙` evening markers;
- uppercase day and MORNING / EVENING labels;
- literal asterisks around headings so WhatsApp renders emphasis;
- the approved heading order;
- blank-line spacing between hierarchy elements and sections;
- the exact `Learn • Think • Verify • Adapt` closing;
- plain-text readability without conversion into tables, cards, or decorative layouts.

Do not silently normalise, compress, expand, or restyle approved spacing and asterisk markers when appending content.

## 13. Gate B - Human daily approval

After generating one day's Morning and Evening content, stop for human review.

The human may approve, reject, or request corrections. The day must not be appended to the weekly text artifact until the human approves it.

## 14. Append and freeze

When the human approves a day and instructs ChatGPT to push or append it, append that approved text to the weekly `.txt` artifact exactly in the approved WhatsApp-ready format.

After append, that day is frozen. Generating a later day must not regenerate, rewrite, reformat, or silently correct an earlier approved day. A frozen day may change only when the human explicitly reopens it.

The weekly artifact therefore grows sequentially:

`Monday -> Tuesday -> Wednesday -> Thursday -> Friday -> Saturday`

Each arrow represents human approval followed by append.

## 15. Final weekly artifact

After Saturday is approved and appended, the weekly `.txt` file becomes the completed human-reviewed learning artifact for that authoring cycle.

The final file must contain only the approved daily content in the approved order and format. Do not rebuild the file from memory when the already approved artifact can be extended directly.

## 16. Human authority

ChatGPT assists with analysis, curriculum proposals, writing, consistency checks, and formatting. It does not replace human curriculum approval.

The human remains the authority for approving Learning Path, Module, and Chapter names and for approving every day's Morning and Evening content before it becomes part of the weekly artifact.
