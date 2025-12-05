# [Module Name]

## Purpose

<!-- What this module accomplishes. Why it exists as a distinct module. -->

## Scope

### In Scope

<!--
Group related items under bold category labels.
Categories should not be headings—they're labels for bullet lists.
-->

**[Category]**:
- [Item]
- [Item]

**[Category]**:
- [Item]
- [Item]

### Out of Scope

<!-- Items explicitly deferred to future phases. -->

**[Category]**:
- [Item] — [reason/phase]

### Exclusions

<!-- Items explicitly NOT supported, even in future. -->

- [Exclusion]: [Rationale]

## Glossary

<!--
Module-specific terms only.
Reader is assumed to know project glossary from 00-overview.md.
-->

**[Term]**: [Definition]

**[Term]**: [Definition]

## Actors

<!--
Actors interact directly with the system to achieve goals.
All actors are stakeholders, but not all stakeholders are actors.
-->

### [Actor Name]

**Goals**:
- [Goal]
- [Goal]

**Characteristics**: [Notable traits relevant to system design]

### [Actor Name]

**Goals**:
- [Goal]
- [Goal]

**Characteristics**: [Notable traits]

### System (Automated)

**Goals**:
- [Automated behavior]
- [Automated behavior]

**Characteristics**: Automated system behaviors that support user goals.

## Use Cases

### Index

<!--
ID structure encodes level:
  UC-[MOD]-J### = Journey (combines multiple goals)
  UC-[MOD]-G### = Goal (user-facing, delivers value)
  UC-[MOD]-T### = Task (subfunctions, reusable steps)
-->

| ID | Name | Level | Primary Actor | Status |
|----|------|-------|---------------|--------|
| UC-[MOD]-J001 | [Name] | Journey | [Actor] | [Draft/Specified/Implemented] |
| UC-[MOD]-G001 | [Name] | Goal | [Actor] | [Draft/Specified/Implemented] |
| UC-[MOD]-G002 | [Name] | Goal | [Actor] | [Draft/Specified/Implemented] |
| UC-[MOD]-T001 | [Name] | Task | [Actor/System] | [Draft/Specified/Implemented] |

---

### Part I: Journeys

<!--
Journeys combine multiple goals into an end-to-end workflow.
Lighter specification—focuses on which goals and why, not step-by-step mechanics.
-->

#### UC-[MOD]-J001: [Journey Name]

##### Summary

<!-- One paragraph: what is this journey and when is it complete? -->

##### Primary Actor

##### Stakeholders and Interests

- **[Stakeholder]**: [What they need from this journey]

##### Goals Involved

<!-- Which goal-level use cases comprise this journey, in typical order -->

| Sequence | Use Case | Required? |
|----------|----------|-----------|
| 1 | UC-[MOD]-G001: [Name] | Yes |
| 2 | UC-[MOD]-G002: [Name] | No |

##### Success Criteria

<!-- What's true when the journey is complete? -->

##### Typical Duration

<!-- Hours? Days? Weeks? -->

##### Variations

<!-- Common alternative paths through the journey -->

---

### Part II: Goals

<!--
Goals are the primary level of specification.
Each goal delivers recognizable value to the primary actor.
Full specification.
-->

#### UC-[MOD]-G001: [Use Case Name]

##### Primary Actor

[Actor name]

##### Stakeholders and Interests

<!--
Who cares about this use case succeeding, and what do they need?
This ensures the use case satisfies all parties, not just the primary actor.
-->

- **[Stakeholder]**: [What they need from this use case]
- **[Stakeholder]**: [What they need from this use case]

##### Preconditions

<!-- What must be true before this use case can begin? -->

- [Condition]

##### Success Guarantee

<!-- What will be true when this use case completes successfully? -->

- [Guarantee]

##### Main Success Scenario

<!--
The "happy path" — numbered steps from trigger to goal.
Each step: [Actor] [action] or [System] [response]
-->

1. [Actor] [does something]
2. System [responds]
3. [Actor] [does something]
4. System [confirms/completes]

##### Extensions

<!--
Branches from the main scenario.
Format: [step number][letter]. [condition]: [what happens]
-->

**2a. [Condition]**:
1. System [alternative behavior]
2. [Return to step X / End use case / etc.]

**3a. [Condition]**:
1. [Alternative flow]

---

### Part III: Tasks

<!--
Tasks are reusable subfunctions called by goal-level use cases.
Minimal specification—these are not user-facing goals.
-->

#### UC-[MOD]-T001: [Task Name]

##### Purpose

<!-- Why this task exists; what goal-level cases use it -->

##### Called By

- UC-[MOD]-G001: [Name] (step 3)
- UC-[MOD]-G002: [Name] (step 2)

##### Input

##### Output

##### Steps

1. [Step]
2. [Step]

##### Failure Modes

- **[Condition]**: [Result]
