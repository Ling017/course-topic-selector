# Course Topic Selector

`course-topic-selector` is a Codex skill for turning source materials into market-fit course topic decisions.

It is designed for cases where a user has notes, drafts, transcripts, outlines, books, or messy teaching materials and needs to answer:

- What course topic should this material become?
- Which audience is most worth targeting?
- What problem does the course actually solve?
- How crowded is the market?
- What competitors or substitutes already solve part of the problem?
- Is the material strong enough to support a real course, or only a lighter product?

## What This Skill Does

This skill combines two constraints:

- `material constraint`: the recommendation must stay inside what the source materials can honestly support
- `market constraint`: the recommendation must reflect real demand, competition, buying logic, and replacement risk

The goal is not to generate catchy titles in isolation.  
The goal is to find the **minimum sellable topic**: a topic the author can truly teach and the market can plausibly buy.

## Best For

Use this skill when you need:

- course topic selection
- market-fit evaluation
- audience targeting
- competitor and substitute analysis
- pricing guidance
- decision-oriented topic reports
- course-readiness evaluation

Do not use it when the topic is already fixed and you only need:

- lesson breakdowns
- lesson scripts
- prompt polishing
- copywriting only

## What Makes It Different

This skill does more than naming and packaging.

It explicitly checks:

- whether the topic comes from real source evidence
- whether users actually have the problem
- whether buyers are more likely to pay for a course, tool, or service
- whether the material has a real teachable kernel versus competitors
- whether the material can support at least 3 meaningful lessons without filler

That last point matters. A topic can sound promising and still fail as a course.  
This skill treats **course-readiness** as a separate decision gate.

## Typical Inputs

- book manuscripts
- course drafts
- founder notes
- workshop transcripts
- research notes
- author archives
- scattered experience documents

Optional supporting inputs:

- author background
- proof of results
- known competitors
- preferred market
- instruction language

## Typical Outputs

- a recommended main topic
- 2 backup directions that are genuinely different
- directions that should not be pursued
- competitor and substitute analysis
- price band
- MVP scope
- 7-day validation plan
- course-readiness judgment
- evidence appendix and traceability

## Output Style

The skill supports both:

- a structured, traceable decision output
- a human-readable decision memo

If the user asks in a specific language, the final report follows that language.  
Market research should include and prioritize markets aligned with that language.

## Core Decision Logic

The skill evaluates course topics through these steps:

1. compress the source material into a real capability core
2. map the material to a real user problem cluster
3. judge market stage and dominant substitutes
4. choose the right packaging and promise ceiling
5. verify course-readiness and lesson-level sufficiency
6. produce a `GO / HOLD / REWORK / NO-GO` recommendation

## Repository Structure

```text
course-topic-selector/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── course-topic-selector.schema.v1.json
    ├── decision-model.md
    ├── decision-report-template.md
    ├── gating-rules.md
    ├── input-contract.md
    ├── market-analysis.md
    └── output-contract.md
```

## Example Prompt

```text
Use $course-topic-selector to evaluate my source materials, compare market demand and competitors, and recommend the best course topic with backups, pricing, and course-readiness checks.
```

## Example Use Cases

- Turn a draft book manuscript into `1 main + 2 backup` course topic directions
- Evaluate whether a founder's notes are strong enough for a paid course
- Compare a potential course against tools, free tutorials, and training camps
- Decide whether the right product form is a full course, workshop, lighter content product, or downgrade

## Why This Repository Exists

Most course topic work fails in one of two ways:

- it follows market heat and loses the author's real edge
- it follows the material too literally and ignores what users actually buy

This skill is built to handle both sides at once, while keeping the recommendation evidence-bound, commercially usable, and readable as a decision document.
