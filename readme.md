# LTM GitHub Copilot Innovation Challenge

## DeliveryPulse - Project Delivery Risk and Action Tracker

### Problem statement
LTM delivery teams manage multiple client projects, milestones, risks, blockers, and action owners. Leadership needs early visibility into delivery risk, while project teams need a simple way to capture issues, track actions, and show progress.

In this hackathon, each team will build **DeliveryPulse**, an end-to-end enterprise application using:

- **.NET Web API** for business logic, APIs, validation, risk scoring, data access, and tests
- **Angular** for the frontend dashboard and user workflows
- **GitHub Copilot-assisted development concepts** including instructions, prompts, skills, agents, MCPs, and hooks
- **Task-based submissions** through the approved submission form after each milestone

By the end, each team should have a working application that demonstrates software design, implementation, testing, quality gates, and responsible GitHub Copilot-assisted development.

---

## Application scope

### Core personas

1. **Delivery Manager** - views project health, risks, blockers, and escalations.
2. **Project Lead** - creates projects, updates milestones, assigns actions, and tracks blockers.
3. **Engineer** - updates assigned actions and adds progress notes.
4. **Reviewer/Admin** - reviews quality, approves closure, and audits changes.

### Core modules

1. Project intake and project list
2. Milestone tracking
3. Risk and blocker management
4. Action item assignment and status tracking
5. Risk scoring engine in .NET
6. Dashboard in Angular
7. Role-based views
8. Audit history
9. Unit, integration, frontend, and end-to-end tests
10. Local quality checks and automation hooks

---

## Suggested technical stack

| Layer | Recommended technology |
|---|---|
| Backend | .NET 8 or later, ASP.NET Core Web API |
| Business logic | Domain services, validators, risk scoring rules |
| Data | EF Core with SQLite or SQL Server LocalDB |
| API docs | Swagger/OpenAPI |
| Frontend | Angular 18 or later |
| UI | Angular Material or Bootstrap |
| Backend tests | xUnit, FluentAssertions, Moq or NSubstitute |
| Frontend tests | Jasmine/Karma or Jest |
| E2E tests | Playwright or Cypress |
| Quality automation | Local scripts for build, lint, format, and tests |
| GitHub Copilot context | Team instructions, reusable prompts, skills, agent workflows, MCP configuration |

---

## Suggested project folder structure

```text
DeliveryPulse
├── src
│   ├── api
│   │   └── DeliveryPulse.Api
│   └── web
│       └── delivery-pulse-web
├── tests
│   ├── DeliveryPulse.Api.Tests
│   └── delivery-pulse-web-e2e
├── docs
│   ├── architecture.md
│   ├── prompt-log.md
│   ├── test-strategy.md
│   └── demo-script.md
├── tools
│   ├── mcp
│   └── quality
├── GitHub
│   ├── instructions.md
│   ├── prompts
│   ├── skills
│   └── agents
└── submissions
```

---

## Innovation challenge format and guidelines

### Team rules

- Participants work in **groups of 3-5 learners**.
- Each group must choose a team name.
- Each task must be completed as a separate milestone.
- Teams must submit evidence after every task and wait for approval before moving to the next task.
- Teams can attend office hours for blockers, design reviews, GitHub Copilot usage guidance, and code review support.
- Teams should maintain their solution folder carefully and NOT to submit anywhere.

### Submission rule after every task

After completing each task, submit the following through the hackathon form:

1. Team name
2. Task number
3. Shared solution folder link or packaged submission link
4. Screenshot of working output
5. Screenshot of test result or quality check result, where applicable
6. Link or screenshot of the updated `docs/prompt-log.md`
7. Short note on what GitHub Copilot capability was used
8. Blockers, assumptions, or reviewer questions

### Approval rule

- Trainers/reviewers will approve or request changes.
- Teams must not start the next task until the previous task is approved.
- If changes are requested, update the task deliverables and resubmit evidence.

---

## Leaderboard scoring

| Category | Points |
|---|---:|
| Task completion | 30 |
| Code quality and maintainability | 15 |
| Business relevance | 15 |
| Test coverage and validation | 15 |
| Effective use of GitHub Copilot concepts | 15 |
| Demo quality and documentation | 10 |
| **Total** | **100** |

Bonus points may be awarded for:

- Clean deployment or demo environment
- Strong accessibility support
- High-quality test automation
- Meaningful use of MCP or agent workflows
- Excellent documentation and prompt discipline

---

# Hackathon tasks

## Task 1 - Team setup, backlog, and solution blueprint

### Objective
Set up the team workspace and define the solution architecture, personas, user stories, and backlog.

### Activities

- Create the team solution folder.
- Add team details in `README.md`.
- Create `docs/architecture.md`.
- Define personas, user journeys, and core modules.
- Create at least 10 user stories in `docs/backlog.md`.
- Create a task tracker in Excel, Planner, Teams Loop, or another organizer-approved tool.

  ### Deliverables

- Updated `README.md`
- `docs/architecture.md`
- `docs/backlog.md`
- Team task tracker

### Evidence to submit

- Screenshot of solution folder structure
- Screenshot of backlog or task tracker
- Link or screenshot of prompt log entry

### Approval criteria

- Architecture is clear.
- User stories are relevant to DeliveryPulse.
- Team workspace is ready for implementation.

---

## Task 2 - Add GitHub Copilot instructions, reusable prompts, and team skills

### Objective
Create shared GitHub Copilot guidance so all team members generate code consistently.

### Activities

- Create `github/instructions.md` with coding standards.
- Add backend standards for .NET APIs, services, validation, error handling, and testing.
- Add frontend standards for Angular components, services, routing, forms, and tests.
- Create reusable prompt files in `github/prompts`, for example:
  - `design-api.prompt.md`
  - `generate-angular-component.prompt.md`
  - `write-unit-tests.prompt.md`
  - `security-review.prompt.md`
  - `refactor-code.prompt.md`
- Create team skill files in `github/skills`, for example:
  - `dotnet-architect.md`
  - `angular-reviewer.md`
  - `test-engineer.md`

### GitHub Copilot focus

- Instructions
- Prompts
- Skills or reusable role-based workflows

### Deliverables

- `GitHub Copilot/instructions.md`
- At least 5 prompt files
- At least 2 reusable skill files

### Evidence to submit

- Screenshot of `github` folder
- Screenshot showing GitHub Copilot using one instruction or prompt file

### Approval criteria

- Instructions are specific to this application.
- Prompt files are reusable and aligned to the application.
- Skills have clear roles and expected outputs.

---

## Task 3 - Scaffold .NET API, Angular app, and baseline build scripts

### Objective
Create the technical foundation for the full-stack application.

### Activities

- Create the .NET Web API project under `src/api/DeliveryPulse.Api`.
- Create the Angular application under `src/web/delivery-pulse-web`.
- Add Swagger/OpenAPI to the backend.
- Add a health check endpoint: `GET /api/health`.
- Add Angular shell with routes for Dashboard, Projects, Risks, Actions, and Admin.
- Add local build scripts for backend and frontend.

### GitHub Copilot focus

- Use GitHub Copilot to scaffold multi-file changes.
- Use prompt files from Task 2.

### Deliverables

- Working .NET API
- Working Angular shell
- Local build scripts

### Evidence to submit

- Screenshot of Swagger page
- Screenshot of Angular home page
- Screenshot of successful local build

### Approval criteria

- Backend and frontend both run locally.
- Build scripts work.
- Application structure follows the agreed architecture.

---

## Task 4 - Implement domain model and business rules

### Objective
Build the core business logic for project delivery risk tracking.

### Activities

Create domain models such as:

- `Project`
- `Milestone`
- `Risk`
- `ActionItem`
- `TeamMember`
- `AuditEntry`

Implement business rules such as:

- Risk score is calculated from impact, probability, due date, and blocker status.
- A project becomes `At Risk` when high-severity risks are open.
- A milestone becomes `Delayed` when due date has passed and status is incomplete.
- An action item cannot be closed without a resolution note.

### GitHub Copilot focus

- Use GitHub Copilot to generate domain models and validators.
- Use GitHub Copilot to explain generated code before submission.

### Deliverables

- Domain entities
- Business services
- Validation logic
- Seed data

### Evidence to submit

- Screenshot of domain model files
- Screenshot of seeded data or API response
- Prompt log entry showing how GitHub Copilot helped design rules

### Approval criteria

- Business logic is implemented in .NET, not only in the UI.
- Risk scoring is testable and clearly separated from controllers.
- Validation rules are meaningful.

---

## Task 5 - Build backend APIs and data access

### Objective
Expose the application features through clean REST APIs.

### Activities

Implement API endpoints for:

- Projects
- Milestones
- Risks
- Action items
- Dashboard summary
- Audit history

Minimum API examples:

```text
GET    /api/projects
POST   /api/projects
GET    /api/projects/{id}
PUT    /api/projects/{id}
GET    /api/projects/{id}/risks
POST   /api/projects/{id}/risks
PUT    /api/risks/{id}/status
GET    /api/dashboard/summary
```

Add:

- EF Core persistence
- DTOs and mapping
- Centralized error handling
- Request validation
- Swagger examples

### GitHub Copilot focus

- Use prompts for API design and controller generation.
- Use GitHub Copilot to generate API examples and error handling patterns.

### Deliverables

- REST APIs
- Data persistence
- Swagger documentation

### Evidence to submit

- Screenshot of Swagger endpoints
- Screenshot of API response with sample data

### Approval criteria

- APIs follow REST conventions.
- Business logic is not duplicated in controllers.
- Error responses are consistent.

---

## Task 6 - Build Angular dashboard and core user flows

### Objective
Create the user interface for project delivery tracking.

### Activities

Build Angular screens for:

- Dashboard summary cards
- Project list
- Project details
- Risk list and risk creation form
- Action item list and status update
- Milestone view

The dashboard should show:

- Total projects
- Projects at risk
- Open high-severity risks
- Overdue actions
- Upcoming milestones

### GitHub Copilot focus

- Use GitHub Copilot to generate Angular components, services, and reactive forms.
- Use reusable frontend prompt files.

### Deliverables

- Angular routes and components
- API integration services
- Forms with validation
- Basic responsive layout

### Evidence to submit

- Screenshot of dashboard
- Screenshot of project detail page
- Screenshot of risk creation form

### Approval criteria

- UI calls real backend APIs.
- Forms validate user input.
- Screens are usable and business-friendly.

---

## Task 7 - Add authentication, roles, audit, and error handling

### Objective
Add enterprise-style controls and traceability.

### Activities

- Add simple authentication or mock login.
- Implement roles:
  - Delivery Manager
  - Project Lead
  - Engineer
  - Admin
- Restrict actions based on role.
- Add audit entries when risks or action items are created, updated, or closed.
- Add frontend error handling and user notifications.

### GitHub Copilot focus

- Use GitHub Copilot to identify authorization gaps.
- Use a security-review prompt before submitting.

### Deliverables

- Role-based access behavior
- Audit history
- Error handling pattern

### Evidence to submit

- Screenshot of role-based screen behavior
- Screenshot of audit history
- Screenshot or copied output from security-review prompt

### Approval criteria

- Role behavior is visible.
- Audit entries are created for important actions.
- Errors are handled gracefully.

---

## Task 8 - Add unit, integration, frontend, and end-to-end tests

### Objective
Prove that the application works and that GitHub Copilot-generated code is validated.

### Activities

Add tests for:

- Risk scoring business rules
- Validators
- API endpoints
- Angular services
- Angular components
- One end-to-end flow, such as creating a project and adding a risk

Minimum expectations:

- Backend unit tests for domain services
- Backend API integration tests
- Frontend component or service tests
- One E2E test

### GitHub Copilot focus

- Use GitHub Copilot to generate test cases from acceptance criteria.
- Use GitHub Copilot to find missing edge cases.

### Deliverables

- Test projects
- Test data builders or fixtures
- Test execution scripts

### Evidence to submit

- Screenshot of backend test results
- Screenshot of frontend test results
- Screenshot of E2E test result

### Approval criteria

- Tests run successfully.
- Tests cover positive and negative scenarios.
- Business rules are validated by automated tests.

---

## Task 9 - Use MCP to connect GitHub Copilot to project context

### Objective
Demonstrate how MCP can provide external or structured context to GitHub Copilot during development.

### Activities

Use an organizer-provided MCP server or create a lightweight local MCP server under `tools/mcp` that exposes useful project context such as:

- Domain glossary
- Sample project and risk data
- API contract summary
- Test data rules
- Architecture decision records

Add MCP setup instructions in `docs/mcp-setup.md`.

Use MCP-backed context to complete one development task, such as:

- Generate additional dashboard test cases
- Review the API contract
- Create sample seed data
- Generate documentation from project metadata

### GitHub Copilot focus

- MCP configuration
- Using external context safely
- Prompting GitHub Copilot with structured project context

### Deliverables

- MCP setup documentation
- MCP server or documented MCP connection
- One feature or test improved using MCP context

### Evidence to submit

- Screenshot of MCP setup
- Screenshot showing GitHub Copilot using MCP context
- Link or screenshot of changed code or tests

### Approval criteria

- MCP usage is clearly demonstrated.
- MCP context is relevant to the application.
- No secrets or private data are exposed.

---

## Task 10 - Use GitHub Copilot agent workflow for a multi-file feature

### Objective
Use agentic development to implement a complete feature across backend, frontend, and tests.

### Activities

Select one feature, such as:

- Risk heatmap dashboard
- Milestone delay prediction indicator
- Bulk action assignment
- Project health export
- Reviewer approval workflow

Use GitHub Copilot Agent Mode or an approved agent workflow to plan and implement the feature.

The feature must include:

- Backend API or business logic change
- Angular UI change
- Tests
- Documentation update

### GitHub Copilot focus

- Agents
- Multi-file implementation
- Review and refinement of generated changes

### Deliverables

- Feature plan in `docs/feature-plan.md`
- Implemented feature
- Tests and documentation

### Evidence to submit

- Screenshot of agent-assisted plan
- Screenshot of working feature
- Screenshot of tests

### Approval criteria

- Feature works end to end.
- Generated code was reviewed and refined by the team.
- Tests prove the feature behavior.

---

## Task 11 - Add hooks, quality gates, and automation scripts

### Objective
Prevent low-quality code from entering the task submission.

### Activities

Add local quality automation:

- formatting script
- linting script
- backend test script
- frontend test script
- pre-submission checklist
- optional local pre-run hook that runs checks before packaging the task submission

Suggested validation behavior:

```text
format-check: verifies backend and frontend formatting
lint-check: runs frontend linting and backend analyzers where available
test-check: runs backend and frontend tests
submission-check: confirms screenshots, prompt log, and docs are updated
```

### GitHub Copilot focus

- Use GitHub Copilot to generate automation scripts.
- Use GitHub Copilot to troubleshoot failing checks.
- Use GitHub Copilot to improve validation scripts.

### Deliverables

- `tools/quality` scripts
- `docs/submission-checklist.md`
- Instructions for running checks locally

### Evidence to submit

- Screenshot of quality scripts running locally
- Screenshot of successful test run
- Screenshot of completed submission checklist

### Approval criteria

- Quality checks are documented.
- Scripts are easy to run.
- Build and tests pass locally.

---

## Task 12 - Final polish, documentation, demo, and showcase submission

### Objective
Prepare the final application for leadership review and scoring.

### Activities

- Update `README.md` with setup and run instructions.
- Add `docs/demo-script.md`.
- Add screenshots of the application.
- Add architecture diagram.
- Add final prompt log summary.
- Add known limitations and future enhancements.
- Prepare a 5-minute demo.

Final demo must show:

1. Dashboard
2. Project creation or selection
3. Risk creation
4. Risk score calculation
5. Action assignment
6. Role-based behavior
7. Tests or quality-check evidence
8. GitHub Copilot artifacts: instructions, prompts, skills, MCP, agents, hooks

### GitHub Copilot focus

- Use GitHub Copilot to improve documentation.
- Use GitHub Copilot to create demo script and reviewer checklist.

### Deliverables

- Final working application
- Complete documentation
- Demo script
- Packaged final submission

### Evidence to submit

- Application screenshots
- Demo video or demo screenshots
- Final test and quality-check screenshot
- Link to final packaged submission
- Link or screenshot of final prompt log

### Approval criteria

- Application runs end to end.
- Documentation is clear.
- Demo is business-relevant.
- All required GitHub Copilot concepts are demonstrated.

---

# Optional bonus tasks

## Bonus Task A - Deploy the application

Deploy the backend and frontend to an approved environment such as Azure App Service, Azure Static Web Apps, IIS, containerized local demo, or another approved platform.

### Evidence

- Deployment URL or recorded demo
- Screenshot of deployed app
- Deployment instructions

---

## Bonus Task B - Add accessibility and performance improvements

Improve the Angular frontend for accessibility and performance.

### Examples

- Keyboard navigation
- Color contrast checks
- ARIA labels
- Lazy-loaded routes
- Loading indicators
- Empty states

### Evidence

- Screenshot of accessibility check
- Screenshot or note on performance improvement

---

# Two-week execution plan

## Before kickoff

- Confirm teams and participants.
- Publish hackathon instructions and task documents.
- Share pre-reads and environment setup checklist.
- Confirm office-hour schedule.
- Confirm reviewers and approval SLA.
- Confirm submission form and evidence requirements.

## Week 1

| Day | Focus | Expected checkpoint |
|---|---|---|
| Day 1 | Kickoff, team setup, architecture | Task 1 approved |
| Day 2 | GitHub Copilot instructions, prompts, skills | Task 2 approved |
| Day 3 | App scaffolding and local build | Task 3 approved |
| Day 4 | Domain model and business rules | Task 4 approved |
| Day 5 | Backend APIs | Task 5 approved |

## Week 2

| Day | Focus | Expected checkpoint |
|---|---|---|
| Day 6 | Angular UI | Task 6 approved |
| Day 7 | Auth, roles, audit | Task 7 approved |
| Day 8 | Testing | Task 8 approved |
| Day 9 | MCP and agent workflow | Tasks 9 and 10 approved |
| Day 10 | Hooks, quality gates, final polish, demo | Tasks 11 and 12 approved |

---

# Office hours plan

Run **3-4 office hours per week**, each for 1 hour.

Suggested agenda:

1. First 10 minutes - common blockers and announcements
2. Next 35 minutes - team-specific Q&A and troubleshooting
3. Next 10 minutes - GitHub Copilot usage tips
4. Last 5 minutes - submission reminders and leaderboard update

---

# Reviewer checklist

Reviewers should check:

- Does the application run locally?
- Is the business logic implemented in .NET?
- Does the Angular UI call real APIs?
- Are tests present and passing?
- Are GitHub Copilot instructions, prompts, skills, agents, MCPs, and hooks demonstrated?
- Are screenshots and prompt logs submitted after each task?
- Is the final demo business-relevant for LTM?

---

# Final definition of done

A team is considered complete when:

- All mandatory tasks are approved.
- The final application runs end to end.
- Backend, frontend, and tests are included.
- Local build, test, and quality checks pass.
- The prompt log is complete.
- GitHub Copilot instructions, prompts, skills, agents, MCPs, and hooks are visible in the submission.
- Final demo and documentation are submitted.
