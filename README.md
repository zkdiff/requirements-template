# Requirements Binder Structure

A modular requirements documentation structure.

## Structure

```
├── 00-overview.md          # Project-level: scope, stakeholders, glossary
│
├── modules/                # One doc per functional module
│   ├── 01-[module].md
│   ├── 02-[module].md
│   └── ...
│
├── reference/              # Cross-cutting technical docs
│   ├── technology.md
│   ├── architecture.md
│   └── design-patterns.md
│
├── governance/             # Constraints and policies
│   └── legal-political-organizational.md
│
└── appendices/
    └── ...
```

## Key Concepts

### Stakeholders vs. Actors

**Stakeholders** (project-level): Anyone with a vested interest in the system's behavior. They have something to gain or lose. Not all stakeholders interact with the system directly.

**Actors** (module-level): Entities that interact directly with the system to achieve a goal. All actors are stakeholders, but not all stakeholders are actors.

### Glossary Splitting

**Project glossary**: Terms that span modules (core entities, acronyms).

**Module glossary**: Terms specific to that module. Readers are assumed to know the project glossary.

### Document Reading Order

1. `00-overview.md` — understand the project
2. `modules/*` — the actual requirements (the "meat")
3. `reference/*` — technical context (supports the modules)
4. `governance/*` — constraints and policies

The reference and governance docs come *after* modules because they're cross-cutting context, not prerequisites.

## Heading Conventions

| Level | Used For |
|-------|----------|
| `#` H1 | Document title (one per file) |
| `##` H2 | Major sections |
| `###` H3 | Subsections |
| `####` H4 | Use case titles, actor names |
| `**Bold**` | Category labels over bullet lists, definition terms |

## Use Case Levels

Use cases are organized into three levels:

| Level | ID Pattern | Purpose |
|-------|------------|---------|
| Journey | `UC-[MOD]-J###` | End-to-end workflows combining multiple goals |
| Goal | `UC-[MOD]-G###` | User-facing use cases that deliver recognizable value |
| Task | `UC-[MOD]-T###` | Reusable subfunctions called by goal-level use cases |

**Journeys** answer "what does the user accomplish over hours/days?"

**Goals** answer "what does the user accomplish in one sitting?"

**Tasks** answer "what does the system do as part of a goal?"

## Use Case Format

Each level has an appropriate level of detail:

**Journey** — lighter touch, focuses on which goals and sequencing:
```markdown
#### UC-[MOD]-J001: [Journey Name]
##### Summary
##### Primary Actor
##### Stakeholders and Interests
##### Goals Involved
##### Success Criteria
##### Typical Duration
##### Variations
```

**Goal** — full specification:
```markdown
#### UC-[MOD]-G001: [Use Case Name]
##### Primary Actor
##### Stakeholders and Interests
##### Preconditions
##### Success Guarantee
##### Main Success Scenario
##### Extensions
```

**Task** — minimal, documents reusable subfunctions:
```markdown
#### UC-[MOD]-T001: [Task Name]
##### Purpose
##### Called By
##### Input
##### Output
##### Steps
##### Failure Modes
```
