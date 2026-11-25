# Project Documentation Guide for Agentic Development

A beginner-friendly guide to understanding, organizing, and maintaining project documentation when building software with AI coding agents.

## 1. Introduction

When building a software project with AI coding agents, writing code is not the only important part.

AI agents need to understand:

- What we are building.
- Why we are building it.
- Who will use the application.
- Which features the application should have.
- Which technologies the project uses.
- How the system should be structured.
- Which coding rules and security requirements must be followed.
- How development tasks should be completed and tested.

Without proper documentation, AI agents may misunderstand requirements, introduce unnecessary technologies, make inconsistent decisions, or write code that does not match the project architecture.

This is why project documentation is an important part of Agentic Development.

**The main goal is to give AI agents and developers a clear understanding of the project before and during development.**

---

## 2. Recommended Project Documentation Structure

A software project does not need dozens of documentation files from the beginning.

We can start with a small number of essential files and gradually add more detailed documentation as the project grows.

Here is the recommended structure for our CSCA Exam Preparation Platform:

```text
csca-platform/
│
├── README.md
├── PRD.md
├── SRS.md
├── AGENTS.md
├── ARCHITECTURE.md
├── SECURITY.md
├── IMPLEMENTATION_PLAN.md
│
├── docs/
│   ├── DATABASE.md
│   ├── API.md
│   ├── DEVELOPMENT.md
│   ├── TESTING-STRATEGY.md
│   ├── ACCEPTANCE_CRITERIA.md
│   ├── TASKS.md
│   ├── DECISIONS.md
│   └── CHANGELOG.md
│
├── frontend/
│   └── AGENTS.md (Optional)
│
└── backend/
    └── AGENTS.md (Optional)
```

Let's understand the purpose of each file.

---

# 3. Essential Root Documentation Files

These files stay in the root directory because they describe the overall project.

## 3.1 README.md

**Purpose:** Introduces the project to developers, contributors, and visitors.

The README is usually the first file someone reads when visiting a GitHub repository.

It should explain what the project is and how someone can understand or start working with it.

### What should it contain?

- Project name and introduction.
- Project goals and objectives.
- Main features overview.
- Technology stack summary.
- Project architecture overview.
- Installation and setup instructions.
- Links to other documentation files.
- Contribution guidelines.

### Why do we need it?

Without a README, new developers may struggle to understand what the repository contains and how to get started.

**Think of README.md as the front page of your project.**

---

## 3.2 PRD.md — Product Requirements Document

**Purpose:** Defines what we are building and why we are building it.

PRD describes the product from a business and user perspective.

It focuses on the product vision, target audience, user problems, and planned features.

### What should it contain?

- Product overview.
- Problem statement.
- Product vision and goals.
- Target audience.
- User roles.
- Core features.
- Feature descriptions.
- User needs and expectations.
- Product scope.
- Out-of-scope features.
- Future improvements.

### Example

Suppose we are building a CSCA Exam Preparation Platform.

The PRD may describe features such as:

- Student registration and login.
- Course enrollment.
- Video lessons.
- PDF learning materials.
- MCQ practice exams.
- Timed mock tests.
- Exam results and performance tracking.
- Leaderboards.
- Admin management.

The PRD explains why these features exist and what value they provide to users.

### Why do we need it?

Without a PRD, developers and AI agents may build features based on assumptions rather than actual product requirements.

**Think of PRD.md as the product blueprint.**

---

## 3.3 SRS.md — Software Requirements Specification

**Purpose:** Defines how the software should behave and what requirements it must satisfy.

While PRD focuses on the product and its features, SRS describes the software requirements in more technical and precise terms.

### What should it contain?

- Functional requirements.
- Non-functional requirements.
- System behaviors.
- User workflows.
- Business rules.
- Input and output requirements.
- Error-handling requirements.
- Performance requirements.
- Compatibility requirements.
- Accessibility requirements.

### Example

A PRD may say:

"Students can take timed mock exams."

The SRS should explain the expected behavior:

- Students can start an available exam.
- The system displays the remaining time.
- Answers are saved according to the defined saving rules.
- The exam is submitted when the timer reaches zero.
- Students can view their results after submission.

These are examples of requirements. Their exact behavior must be finalized during product planning.

### Why do we need it?

Without an SRS, AI agents may implement the same feature differently because its expected behavior is not clearly defined.

**Think of SRS.md as the software behavior specification.**

---

## 3.4 AGENTS.md — AI Agent Instructions

**Purpose:** Provides instructions and guidelines to AI coding agents working on the project.

This is one of the most important files in Agentic Development.

It helps AI agents understand how they should work within the project.

### What should it contain?

- Project context.
- Important documentation references.
- Coding conventions.
- Naming conventions.
- Folder and file organization rules.
- Technology restrictions.
- Development guidelines.
- Testing requirements.
- Security instructions.
- Git and commit guidelines.
- Rules for modifying existing code.
- Instructions for asking before making major changes.

### Example

```markdown
# AI Agent Instructions

## Before Starting Work

Read the following documentation:

1. README.md
2. PRD.md
3. SRS.md
4. ARCHITECTURE.md
5. SECURITY.md
6. IMPLEMENTATION_PLAN.md

Read additional documentation when it is
relevant to the task.

## Development Rules

- Follow the existing project architecture.
- Use the technologies defined in ARCHITECTURE.md.
- Follow the requirements in SRS.md.
- Follow all applicable security rules.
- Do not introduce unnecessary dependencies.
- Do not modify unrelated code.
- Run relevant tests after making changes.
- Explain important changes before completing a task.
```

### Important: Different AI Tools Use Different Instruction Files

There is no single filename that every AI coding tool automatically reads.

Examples include:

| AI Coding Tool | Common Instruction File |
|---|---|
| OpenAI Codex | AGENTS.md |
| Claude Code | CLAUDE.md |
| Cursor | .cursor/rules/ |
| GitHub Copilot | .github/copilot-instructions.md |

We can maintain AGENTS.md as the main source of project-wide instructions and create small tool-specific instruction files when needed.

Do not duplicate all instructions unnecessarily.

### Why do we need it?

Without clear instructions, AI agents may use inconsistent coding styles, ignore project conventions, or make unnecessary architectural changes.

**Think of AGENTS.md as the working guidelines for AI coding agents.**

---

## 3.5 ARCHITECTURE.md — System Architecture

**Purpose:** Explains how the application is technically structured and how its components work together.

It describes the technologies, system components, and overall technical design.

### What should it contain?

- Technology stack.
- Frontend architecture.
- Backend architecture.
- Database technology.
- Authentication solution.
- Third-party services.
- Project folder structure.
- System components.
- Data flow.
- Integration between frontend and backend.
- Architectural rules and constraints.

### Example

For our CSCA Platform, the architecture may include:

| Area | Technology |
|---|---|
| Frontend | Next.js, React, TypeScript |
| Styling | Tailwind CSS, Hero UI |
| Backend | Node.js, Express.js, TypeScript |
| Database | PostgreSQL |
| Database ORM | Prisma |
| Database Hosting | Neon |
| Authentication | Better Auth |
| Validation | Zod |
| File Storage | Cloudflare R2 |

These are proposed project technologies. Any technology that has not been finalized should be marked as a proposal.

### Why do we need it?

Without architecture documentation, AI agents may introduce incompatible technologies, duplicate responsibilities, or create an inconsistent system structure.

**Think of ARCHITECTURE.md as the technical blueprint of the application.**

---

## 3.6 SECURITY.md — Security Requirements

**Purpose:** Defines the security rules and requirements that developers and AI agents must follow.

Security should be considered throughout development, not added at the end.

### What should it contain?

- Authentication requirements.
- Authorization requirements.
- Role-based access control (RBAC).
- Password and session security.
- API protection.
- Input validation.
- Data protection.
- File upload security.
- Rate limiting.
- Secure error handling.
- Environment variable and secret management.
- Logging and audit requirements.
- Backup and recovery requirements.

### Example

For our CSCA Platform:

- Students must not access admin-only resources.
- Authorization must be enforced on the server.
- Sensitive credentials must never be committed to GitHub.
- File access must follow the defined permission rules.
- User input must be validated.
- Authentication and session handling must follow secure practices.

### Why do we need it?

Without security documentation, AI agents may implement features without considering important security risks.

**Think of SECURITY.md as the security rulebook of the application.**

---

## 3.7 IMPLEMENTATION_PLAN.md — Development Roadmap

**Purpose:** Defines how the project will be developed, step by step.

It explains the order of implementation and helps developers and AI agents understand what should be built first.

### What should it contain?

- Development phases.
- Major milestones.
- Feature implementation order.
- Task dependencies.
- Development priorities.
- Expected deliverables.
- Completion conditions.

### Example

A simplified development plan:

**Phase 1: Project Foundation**
- Repository setup.
- Frontend and backend initialization.
- Environment configuration.
- Basic architecture setup.

**Phase 2: Core Backend**
- Database setup.
- Authentication.
- User and role management.
- Core API development.

**Phase 3: Frontend Development**
- Application layout.
- Dashboard.
- Course interfaces.
- Exam interfaces.

**Phase 4: Integration**
- Frontend and backend integration.
- Data handling.
- Error handling.

**Phase 5: Testing and Deployment**
- Functional testing.
- Security testing.
- Performance checks.
- Production deployment.

The actual implementation order should follow the approved project strategy.

### Why do we need it?

Without an implementation plan, AI agents may work on features in the wrong order or start tasks before their dependencies are ready.

**Think of IMPLEMENTATION_PLAN.md as the development roadmap.**

---

# 4. Supporting Documentation Inside docs/

The root files provide the overall project context.

The docs/ directory contains more detailed technical documentation.

We do not need to create every supporting file immediately. Add them when the project requires more detailed specifications.

## 4.1 DATABASE.md

**Purpose:** Documents the database design.

### What should it contain?

- Database technology.
- Table definitions.
- Entity relationships.
- Field names and data types.
- Primary keys and foreign keys.
- Constraints.
- Indexes.
- Database rules.
- Migration guidelines.

### Example

A Student entity may contain:

- id
- name
- email
- createdAt

The actual database schema should be designed and finalized before documenting exact fields and relationships.

**Why is it useful?**

It helps developers and AI agents understand how data is stored and how different entities relate to each other.

---

## 4.2 API.md

**Purpose:** Documents how the frontend and backend communicate.

### What should it contain?

- API overview.
- Endpoint URLs.
- HTTP methods.
- Request parameters.
- Request body examples.
- Response formats.
- Authentication requirements.
- Error responses.
- API versioning rules.

### Example

```text
GET /api/courses

Purpose:
Retrieve available courses.

Authentication:
Depends on the approved access policy.

Response:
A list of available courses.
```

**Why is it useful?**

It prevents frontend and backend developers from making different assumptions about API behavior.

---

## 4.3 DEVELOPMENT.md

**Purpose:** Explains how to set up and run the project locally.

### What should it contain?

- Prerequisites.
- Installation steps.
- Environment configuration.
- Dependency installation.
- Database setup.
- Development commands.
- Local server instructions.
- Troubleshooting guidance.

### Why is it useful?

New developers can set up the project without repeatedly asking how to run it.

---

## 4.4 TESTING-STRATEGY.md

**Purpose:** Defines how the application should be tested.

### What should it contain?

- Testing approach.
- Unit testing.
- Integration testing.
- End-to-end testing.
- API testing.
- Security testing.
- Test environment.
- Testing tools.
- Test coverage expectations.
- Regression testing.

### Example

For an exam submission feature, tests may verify:

- A student can submit an exam.
- An invalid submission is rejected.
- The submitted answers are saved correctly.
- A student cannot submit another student's exam.

**Why is it useful?**

It helps verify that AI-generated code actually works instead of relying only on the agent's claims.

---

## 4.5 ACCEPTANCE_CRITERIA.md

**Purpose:** Defines the conditions that must be satisfied before a feature is considered complete.

### What should it contain?

- Feature completion requirements.
- Expected behavior.
- Validation conditions.
- Error scenarios.
- User permission requirements.
- Testing conditions.

### Example

Feature: Student Registration

Acceptance criteria:

- A user can register with valid information.
- Invalid email addresses are rejected.
- Duplicate accounts are handled correctly.
- Password requirements are enforced.
- The registration flow provides appropriate feedback.

**Why is it useful?**

It gives developers and AI agents a clear definition of what "complete" actually means.

---

## 4.6 TASKS.md

**Purpose:** Tracks development tasks and their progress.

### What should it contain?

- Task name.
- Task description.
- Priority.
- Dependencies.
- Current status.
- Related features.

### Example

```markdown
# Development Tasks

## Authentication

- [ ] Set up authentication.
- [ ] Implement registration.
- [ ] Implement login.
- [ ] Implement logout.
- [ ] Add role-based authorization.
```

**Why is it useful?**

It helps developers and AI agents understand which tasks are pending, ongoing, or completed.

For larger projects, a dedicated issue tracker or project management tool may be more suitable.

---

## 4.7 DECISIONS.md

**Purpose:** Records important technical decisions and the reasons behind them.

### What should it contain?

- Decision title.
- Date.
- Problem or context.
- Available options.
- Selected solution.
- Reason for selection.
- Consequences of the decision.

### Example

```markdown
# Technical Decisions

## Database Selection

Decision:
Use PostgreSQL.

Reason:
The application needs relational data
and structured relationships.

Selected ORM:
Prisma.
```

**Why is it useful?**

When developers or AI agents revisit an architectural decision, they can understand why it was made instead of making the same discussion from the beginning.

For a larger project, these decisions can later be organized into separate Architecture Decision Records (ADRs).

---

## 4.8 CHANGELOG.md

**Purpose:** Maintains a history of important project changes.

### What should it contain?

- Version or release.
- Date.
- Added features.
- Changed features.
- Fixed issues.
- Removed features.
- Important technical updates.

### Example

```markdown
# Changelog

## [Unreleased]

### Added
- Initial project setup.

### Changed
- No changes yet.

### Fixed
- No fixes yet.
```

**Why is it useful?**

It helps developers understand how the project has evolved over time.

---

# 5. Optional Frontend and Backend AGENTS.md Files

Our project has two main development areas:

- frontend/
- backend/

The root AGENTS.md can provide instructions for the entire project.

However, frontend and backend may have different coding rules and development requirements.

When necessary, we can create additional instruction files:

```text
frontend/
└── AGENTS.md

backend/
└── AGENTS.md
```

### frontend/AGENTS.md

Can contain:

- React and Next.js coding rules.
- Component organization.
- Styling conventions.
- State management rules.
- Form handling guidelines.
- Frontend testing requirements.

### backend/AGENTS.md

Can contain:

- Express.js coding rules.
- API structure.
- Controller and service organization.
- Database access rules.
- Validation requirements.
- Backend testing requirements.
- Server-side security rules.

These files should contain additional instructions, not copies of all the root instructions.

AI tools that support hierarchical AGENTS.md files can apply more specific instructions to the relevant directories. Always check the behavior of the particular tool being used.

---

# 6. How Documentation Files Work Together

Documentation files should not work independently.

Each file has a specific responsibility, and together they provide the complete project context.

Here is a simplified relationship:

```text
                  README.md
                      |
                      v
                    PRD.md
                      |
                      v
                    SRS.md
                      |
                      v
               ARCHITECTURE.md
                      |
             +--------+--------+
             |                 |
             v                 v
         DATABASE.md       SECURITY.md
             |                 |
             +--------+--------+
                      |
                      v
                 AGENTS.md
                      |
                      v
            IMPLEMENTATION_PLAN.md
                      |
                      v
               DEVELOPMENT WORK
                      |
             +--------+--------+
             |                 |
             v                 v
         TESTING.md         TASKS.md
```

This is a conceptual relationship, not a mandatory execution sequence.

For example:

- PRD defines what the product should provide.
- SRS defines the expected software behavior.
- ARCHITECTURE explains how the system is structured.
- DATABASE explains how data is organized.
- SECURITY defines the security requirements.
- AGENTS tells AI agents which instructions and documentation to follow.
- IMPLEMENTATION_PLAN defines the development order.
- TESTING_STRATEGY explains how the implementation will be verified.

---

# 7. Referencing Documentation Instead of Duplicating Information

One important documentation practice is maintaining a **Single Source of Truth**.

It means each type of information should have one main location where it is maintained.

Other files should reference that location instead of copying the same information.

### Example 1: Technology Stack

The technology stack is maintained in ARCHITECTURE.md.

```markdown
# ARCHITECTURE.md

## Frontend
- Next.js
- React
- TypeScript

## Backend
- Node.js
- Express.js
- TypeScript
```

Now DEVELOPMENT.md can reference it:

```markdown
# DEVELOPMENT.md

## Technology Stack

The project technology stack is defined in:

[ARCHITECTURE.md](../ARCHITECTURE.md)

Review the architecture documentation before
setting up the development environment.
```

### Example 2: AI Agent Instructions

AGENTS.md can tell the AI agent to read the relevant documentation:

```markdown
# AGENTS.md

## Before Development

Read the following files:

- PRD.md
- SRS.md
- ARCHITECTURE.md
- SECURITY.md

Follow all applicable requirements and rules
defined in these documents.

For database-related tasks, also read:

- docs/DATABASE.md

For API-related tasks, also read:

- docs/API.md
```

### Why is this useful?

Suppose we change the authentication technology.

Instead of updating the same information in five different files, we update its canonical definition in ARCHITECTURE.md and update any other documentation that actually depends on the changed decision.

This reduces:

- Duplicate information.
- Conflicting documentation.
- Unnecessary updates.
- Confusion for developers and AI agents.

**Important:** Referencing a file does not automatically enforce its rules. The AI agent must actually read the relevant file, and important requirements must also be verified through tests, code review, and CI checks.

---

# 8. How to Create Documentation Without Overcomplicating the Project

We should not create all documentation files at once.

Documentation should grow with the project.

A practical approach is to divide the work into three phases.

## Phase 1: Project Foundation

Create these files first:

1. README.md
2. PRD.md
3. SRS.md
4. ARCHITECTURE.md
5. SECURITY.md
6. AGENTS.md
7. IMPLEMENTATION_PLAN.md

At this stage, the goal is to establish the product requirements, technical direction, and AI working instructions.

## Phase 2: Technical Documentation

As the architecture becomes clearer, create:

1. DATABASE.md
2. API.md
3. DEVELOPMENT.md
4. TESTING-STRATEGY.md
5. ACCEPTANCE_CRITERIA.md

At this stage, the goal is to document the technical details needed for implementation.

## Phase 3: Development Tracking

During implementation, maintain:

1. TASKS.md
2. DECISIONS.md
3. CHANGELOG.md

Add more documentation only when necessary.

**Remember:** These phases describe the order of documentation work. They are not additional folders or files.

---

# 9. Important Documentation Best Practices

Follow these practices throughout development:

### 1. Keep Documentation Updated

Documentation should reflect the current project requirements and architecture.

If a feature changes, update the relevant documentation.

### 2. Avoid Duplicate Information

Maintain one main source of truth for each type of information.

Use references instead of copying the same content.

### 3. Write Clear Instructions

AI agents work better when instructions are specific, understandable, and actionable.

Avoid vague instructions such as "write clean code."

Instead, explain the expected coding conventions and requirements.

### 4. Do Not Make Unapproved Architectural Changes

AI agents should not introduce major dependencies, replace technologies, or redesign important system components without following the project's decision-making process.

### 5. Verify AI-Generated Code

Never assume generated code is correct simply because an AI agent says the task is complete.

Use tests, code review, and security checks.

### 6. Keep Security in Mind

Security requirements should be considered during planning, implementation, and testing.

### 7. Create Documentation When Needed

Not every project needs every documentation file.

Start with essential files and add more when the complexity of the project requires them.

---

# 10. Final Checklist

Before starting serious development, check whether the project has the necessary foundation.

- [ ] Project introduction is documented.
- [ ] Product goals and scope are defined.
- [ ] Functional requirements are documented.
- [ ] Non-functional requirements are documented.
- [ ] Technology stack is defined.
- [ ] System architecture is documented.
- [ ] Security requirements are defined.
- [ ] AI agent instructions are available.
- [ ] Development phases are planned.
- [ ] Relevant database and API documentation is available.
- [ ] Testing and acceptance requirements are defined.

Not every supporting document must exist before development begins. The goal is to have enough accurate documentation for the work being performed.

---

# Conclusion

Agentic Development is not simply about asking AI to write code.

It is about giving AI agents the right context, requirements, instructions, tools, and boundaries so they can contribute effectively to software development.

Well-organized documentation helps both developers and AI agents understand the project, make consistent decisions, and maintain code quality as the application grows.

**Build with a clear plan. Give agents the right context. Verify the results. Stay in control of the development process.**
