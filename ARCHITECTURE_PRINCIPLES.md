# Project Brain — Architecture Principles

**Status:** Active  
**Scope:** Project Brain Platform  
**Purpose:** Define the core architecture principles that govern the design, evolution, and operation of Project Brain.

---

## 1. Mission

Project Brain is a platform designed to support the controlled creation, documentation, evolution, and maintenance of complex projects and applications.

Its purpose is to provide:

- structured project memory;
- controlled documentation management;
- traceability between requirements, decisions, risks, code and releases;
- AI-assisted analysis and proposal generation;
- human validation before implementation;
- controlled change implementation;
- reusable governance across multiple projects.

---

## 2. Core Principles

### Principle 1 — Projects are data, not code

Projects must be represented as structured data.

The application must not require code changes to add or manage a new project.

Correct approach:

```text
projects
domains
documents
specifications
trace links
statuses
```

The user interface must render project information from structured data sources.

---

### Principle 2 — Spec-driven change

Every meaningful change must be linked to a specification, decision, or formal work order.

Before implementation, each change must answer:

```text
Why is this change required?
Which requirement, specification, or decision justifies it?
Which project, domain, document, data object or code object is impacted?
```

No significant change should be implemented without a documented reason.

---

### Principle 3 — Data-driven interface

The interface must be generated from structured data wherever possible.

Menus, project structures, domains, documents, statuses and relationships should not be manually hardcoded for each use case.

The platform must remain reusable across different projects.

---

### Principle 4 — Traceability-first architecture

Project Brain must maintain traceability between key objects:

```text
project
domain
specification
document
decision
risk
impact
release
code object
test
audit event
```

The platform must be able to explain:

```text
Why something exists
Where it is documented
Which decision supports it
Which risks are linked to it
Which code implements it
Which tests validate it
Which release delivered it
Who validated it
When it changed
```

---

### Principle 5 — AI is controlled, not autonomous

AI may assist with:

- analysis;
- drafting;
- impact assessment;
- proposal generation;
- code suggestions;
- documentation updates;
- test suggestions.

AI must not make final decisions autonomously.

AI must not modify production systems directly.

All AI-generated proposals must be reviewed, accepted, corrected or rejected by a human validator.

---

### Principle 6 — AI requires a controlled context

AI must not operate from vague or incomplete prompts.

Before any AI-assisted work, Project Brain must prepare a structured context package containing:

- the objective;
- relevant project data;
- applicable specifications;
- related documents;
- existing decisions;
- known risks;
- relevant code context;
- data model context;
- architectural constraints;
- expected output format;
- allowed and forbidden actions.

The AI response must be structured and reviewable.

---

### Principle 7 — Controlled implementation workflow

A validated proposal must be implemented through a controlled process.

Code changes must follow this workflow:

```text
work order
context package
AI or human proposal
impact analysis
human validation
branch creation
file changes
pull request
tests and build
preview
approval
merge
release
audit
```

No code change should be applied directly to production.

---

### Principle 8 — Documentation and code must stay connected

A feature or change is incomplete if only the code exists.

Each implemented capability should be connected to:

- a specification or work order;
- related documentation;
- relevant decisions;
- related risks;
- data model elements;
- code objects;
- tests;
- release notes;
- audit events.

Documentation must not be an afterthought. It is part of the system.

---

### Principle 9 — Platform self-governance

Project Brain must be governed using the same principles it applies to other projects.

Its own evolution must be managed through:

- specifications;
- architecture documentation;
- decisions;
- risks;
- releases;
- audit events;
- controlled implementation workflows.

The platform must remain understandable, maintainable and traceable over time.

---

### Principle 10 — Reusability before shortcuts

Project Brain must be designed as a reusable platform.

Project-specific shortcuts must be avoided when they weaken the generic architecture.

A solution is acceptable only if it can be reused, extended or adapted without breaking the core platform design.

---

## 3. Architecture Layers

Project Brain should be structured around clear architectural layers:

```text
Interface Layer
Application / Use Case Layer
Domain Layer
Data Layer
Documentation Layer
Code Intelligence Layer
AI Context Layer
Implementation Control Layer
Validation and Release Layer
Infrastructure Layer
```

Each layer must have a clear responsibility.

Business logic must not be mixed directly into the interface layer.

Integration logic must not be mixed with domain logic.

---

## 4. Release Gate

Before any release, the following questions must be answered:

```text
1. Which specification, decision or work order justifies this release?
2. Which architecture principle does it support?
3. Does it introduce hardcoded project-specific logic?
4. Does it improve structured memory or traceability?
5. Are impacted documents identified?
6. Are impacted data objects identified?
7. Are impacted code objects identified?
8. Is human validation required and recorded?
9. Are tests, build checks or validation steps defined?
10. Is rollback possible?
11. Is the release documented?
12. Is an audit trace created?
```

If any answer is unclear or weak, the release must be reviewed before implementation.

---

## 5. Definition of Done

A change is considered complete only when:

```text
1. The reason for the change is documented.
2. The related specification, decision or work order is identified.
3. Impacted documents are updated or reviewed.
4. Impacted data objects are identified.
5. Impacted code objects are identified.
6. Traceability links are created or updated.
7. Tests or validation steps are defined.
8. Human validation is recorded.
9. Release notes are updated.
10. Audit history is created.
```

---

## 6. Short Rule

```text
No magic.
No hardcoding.
No AI without context.
No code without version control.
No change without traceability.
No release without validation.
```
