# Project Brain — Definition of Done

**Status:** Active  
**Scope:** Project Brain Platform  
**Purpose:** Define the minimum conditions required before any change, feature, document, release or implementation can be considered complete.

---

## 1. General Rule

A change is not complete simply because it works visually.

A change is complete only when it is:

- justified;
- documented;
- traceable;
- validated;
- versioned;
- testable;
- auditable;
- aligned with the platform architecture principles.

---

## 2. Required Conditions

Every meaningful change must satisfy the following conditions.

### 2.1 Reason

The reason for the change must be documented.

The change must answer:

```text
Why is this needed?
What problem does it solve?
Who or what benefits from it?
```

---

### 2.2 Link to a Specification, Decision or Work Order

The change must be linked to at least one of the following:

- specification;
- architecture decision;
- business decision;
- work order;
- risk mitigation;
- release objective.

No major change should exist without a clear justification.

---

### 2.3 Documentation Updated

Any impacted documentation must be created or updated.

Documentation may include:

- product vision;
- architecture documentation;
- data model;
- API contract;
- business rules;
- user workflow;
- implementation notes;
- release notes.

---

### 2.4 Traceability Updated

Traceability links must be created or updated when relevant.

A change should be linkable to:

```text
project
domain
specification
document
decision
risk
impact
data object
code object
test
release
audit event
```

---

### 2.5 Data Impact Reviewed

If the change affects data, the impacted data objects must be identified.

This includes:

- tables;
- fields;
- relationships;
- statuses;
- migrations;
- permissions;
- data retention;
- audit requirements.

---

### 2.6 Code Impact Reviewed

If the change affects code, the impacted code objects must be identified.

This includes:

- files;
- modules;
- functions;
- API endpoints;
- services;
- repositories;
- UI components;
- tests;
- configuration;
- deployment settings.

---

### 2.7 AI Output Reviewed

If AI is used, the AI output must be reviewed before implementation.

AI-generated output must be:

- structured;
- understandable;
- linked to the work order;
- reviewed by a human;
- accepted, corrected or rejected.

AI must not directly modify production systems.

---

### 2.8 Validation Completed

Validation must be appropriate to the type of change.

Examples:

```text
Documentation change -> review and approval
Data change -> migration reviewed
Code change -> branch, pull request, tests, build, preview
Architecture change -> decision record and impact analysis
AI proposal -> human validation
```

---

### 2.9 Version Control

Any code change must be versioned in GitHub.

A code change must follow:

```text
branch
pull request
review
tests/build
preview
merge
release
```

No direct production modification is allowed.

---

### 2.10 Audit Created

An audit trace must be created for meaningful changes.

The audit should capture:

- what changed;
- why it changed;
- who validated it;
- when it changed;
- what was impacted.

---

## 3. Definition of Done Checklist

A change is done only if the following checklist is satisfied:

```text
[ ] Reason documented
[ ] Related spec, decision or work order identified
[ ] Impacted documents reviewed
[ ] Impacted data objects reviewed
[ ] Impacted code objects reviewed
[ ] Traceability links updated
[ ] AI output reviewed if AI was used
[ ] Human validation recorded
[ ] Tests or validation steps completed
[ ] Release notes updated if needed
[ ] Audit event created
[ ] Rollback or correction path identified
```

---

## 4. Special Rule for Code Changes

A code change is done only if:

```text
[ ] Code is committed in GitHub
[ ] Change is done in a separate branch
[ ] Pull Request exists
[ ] Build succeeds
[ ] Tests pass or validation is documented
[ ] Preview is available when relevant
[ ] Human approval is recorded
[ ] Merge is controlled
[ ] Release note is updated
```

---

## 5. Short Rule

```text
If it is not documented, linked, validated and traceable, it is not done.
```
