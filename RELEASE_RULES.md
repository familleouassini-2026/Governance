# Project Brain — Release Rules

**Status:** Active  
**Scope:** Project Brain Platform  
**Purpose:** Define the mandatory rules for preparing, validating, releasing and auditing changes.

---

## 1. General Rule

A release must not be treated as a simple deployment.

A release is a controlled delivery that must be:

- justified;
- documented;
- traceable;
- validated;
- reversible where possible;
- linked to the platform governance.

---

## 2. Release Types

Project Brain may use the following release types:

```text
Foundation
Feature
Bugfix
Refactoring
Architecture
Documentation
Security
Data Model
AI Workflow
Infrastructure
```

Each release must clearly state its type.

---

## 3. Release Requirements

Before a release is allowed, the following must be identified:

```text
1. Release objective
2. Related specification, decision or work order
3. Impacted documents
4. Impacted data objects
5. Impacted code objects
6. Required validation steps
7. Risks
8. Rollback or correction path
```

---

## 4. Code Release Rule

Any release involving code must follow:

```text
branch
pull request
build
tests or documented validation
preview when relevant
human approval
merge
deployment
audit
```

Direct modification of production is not allowed.

---

## 5. AI-Assisted Release Rule

If AI is used in a release, the release must record:

```text
AI work order
context package used
AI proposal
human validation
accepted changes
rejected changes if any
```

AI-generated output must not be applied without review.

---

## 6. Documentation Rule

A release is incomplete if the documentation is not updated when relevant.

Documentation may include:

```text
architecture principles
definition of done
data model
API contract
workflows
decision records
release notes
audit history
```

---

## 7. Release Gate Checklist

A release can proceed only if this checklist is satisfied:

```text
[ ] Release objective is clear
[ ] Release type is identified
[ ] Related spec, decision or work order is linked
[ ] Impacted documents are identified
[ ] Impacted data objects are identified
[ ] Impacted code objects are identified
[ ] Validation steps are defined
[ ] Human validation is recorded
[ ] Rollback or correction path is identified
[ ] Release notes are prepared
[ ] Audit event will be created
```

---

## 8. Release Note Minimum Content

Each release note should include:

```text
Version
Date
Release type
Objective
Changes delivered
Documents impacted
Data impacted
Code impacted
Validation performed
Known limits
Rollback or correction path
Next step
```

---

## 9. Short Rule

```text
No release without reason.
No release without validation.
No release without trace.
```
