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

`Weekly Intelligence -> repository inspection -> curriculum comparison -> Learning Path / Module / six-Chapter proposal -> human review -> day-specific content -> human review -> append approved content -> final weekly text file`

Human approval is required at both the curriculum-structure stage and the day-specific content stage. ChatGPT must stop at each gate instead of silently continuing.

## 4. Stage A - Weekly Intelligence input

The human pastes or supplies the completed Weekly Intelligence in ChatGPT.

Before proposing curriculum, ChatGPT must read the current applicable repository standards and inspect the existing curriculum available in the repository. Chat memory or an earlier AI summary must not be treated as the only source of truth.

## 5. Stage B - Curriculum proposal only

ChatGPT analyses the Weekly Intelligence, identifies its durable human meaning, compares it with the existing curriculum, and proposes only the curriculum structure needed for human review.

At this stage the output is limited to:

- Learning Path name;
- Module name;
- exactly six Chapter names.

From Weekly Intelligence 016 onward, every weekly curriculum proposal must derive six distinct Chapters from the supplied Weekly Intelligence. The six Chapters must form a coherent progression within the approved Module. They must not be filler, artificial subdivisions, or repetitions created only to satisfy the required count.

If the Weekly Intelligence does not contain enough durable learning substance to support six meaningful Chapters without lowering the curriculum standard, ChatGPT must stop and identify that conflict for human review rather than invent weak Chapters.

Do not generate morning content, evening content, exercises, explanations, or the weekly text file at this stage.

## 6. Curriculum quality checks

Before presenting a proposal, check:

- Durability: does it develop a lasting human capability rather than merely describe this week's technology or news?
- Hierarchy: do the six Chapters belong to the Module, and does the Module belong to the Learning Path?
- Progression: do the six Chapters build naturally rather than repeat one another?
- Distinctness: does each of the six Chapters have its own meaningful learning responsibility?
- Human meaning: is the capability people should strengthen clear?
- Grounding: can every Chapter be traced back to the Weekly Intelligence?
- Existing curriculum: does the proposal avoid unnecessary duplication?
- Pillars: does it meaningfully support Learn, Think, Verify, or Adapt?

The six-Chapter requirement must never be used to justify weak, duplicated, or unsupported curriculum. If six meaningful Chapters cannot be derived while satisfying these checks, stop for human review.

## 7. Gate A - Human curriculum approval

After presenting the Learning Path, Module, and six Chapter names, stop.

The human may approve, reject, or request changes. No day-specific learning content may be generated until the curriculum structure is approved.

Once approved, the Learning Path, Module, and six Chapter names become the working structure for that weekly authoring cycle unless the human explicitly reopens the decision.

## 8. Stage C - Generate one day at a time

After curriculum approval, generate only the requested day's content. Start with Monday Morning and Monday Evening unless the human explicitly requests another approved day.

Do not generate later days automatically. Each day has its own human review gate.

Monday through Saturday map in order to the six approved Chapters: Monday uses Chapter 01, Tuesday Chapter 02, Wednesday Chapter 03, Thursday Chapter 04, Friday Chapter 05, and Saturday Chapter 06.

## 9. Morning content structure

For Monday through Saturday, morning content uses this order:

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

For Monday through Saturday, evening content uses this order:

`🌙 <DAY> EVENING`

`*Learning Path <number> – <name>*`

`*Module <number> – <name>*`

`*Chapter <number> – <name>*`

`*Looking Back*`

`*Thinking Together*`

`*Moving Forward*`

`*Learn • Think • Verify • Adapt*`

Evening content must add reflection and meaning rather than simply repeat the morning message.

## 11. Saturday chapter and weekly integration

Saturday uses Chapter 06 of the approved six-Chapter progression. Its learning content should complete the week's progression while also helping us connect and integrate the ideas developed across the week.

Saturday must remain grounded in its approved Chapter rather than becoming an unrelated extra topic. Its role as the sixth Chapter does not remove the need for weekly reflection and integration where those elements naturally support the Chapter.

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

### Mandatory weekly artifact filename

From Weekly Intelligence 016 onward, the weekly curriculum text artifact must use only the exact Monday-to-Saturday date range as its filename.

Required format:

`DD Mon YYYY - DD Mon YYYY.txt`

Example for Weekly Intelligence 016:

`WI-016/02 Nov 2026 - 07 Nov 2026.txt`

Within each `WI-XXX` directory, do not create or retain a generic weekly curriculum filename such as `week.txt`, `weekly.txt`, `final.txt`, or another alias for the same approved weekly artifact. The date-range `.txt` file is the single authoritative weekly curriculum artifact.

The first date must be that curriculum week's Monday and the second date must be its Saturday. Use two-digit day numbers, three-letter English month names, four-digit years, spaces around the hyphen, and the lowercase `.txt` extension exactly as shown.

## 16. Human authority

ChatGPT assists with analysis, curriculum proposals, writing, consistency checks, and formatting. It does not replace human curriculum approval.

The human remains the authority for approving Learning Path, Module, and all six Chapter names and for approving every day's Morning and Evening content before it becomes part of the weekly artifact.
