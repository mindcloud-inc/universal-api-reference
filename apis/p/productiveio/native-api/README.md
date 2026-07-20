# Productive.io: Native API Reference

A consolidated summary of Productive.io's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://developer.productive.io/
- **API base URL:** `https://api.productive.io/api/v2`

## Authentication

### Productive API token

Authenticate with Productive using X-Auth-Token and X-Organization-Id headers.

### Credentials

- **API Key:** `apiKey` · required · Productive personal access token.
- **Organization ID:** `organizationId` · required · Numeric Productive organization ID.

Send these headers with each API request:

```http
X-Auth-Token: <apiKey>
X-Organization-Id: <organizationId>
```

[Official authentication documentation](https://developer.productive.io/index.html#header-authorization)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.api+json` |
| `Content-Type` | `application/vnd.api+json` |

Responses from this API use JSON. Response data is read from `data`. The total page count is read from `meta.total_pages`. The current page number is read from `meta.current_page`.

## Pagination

Use `page[size]` in the query string to set the page size (default 30; accepted range 1–200). Use `page[number]` in the query string to choose the page; numbering starts at 1.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Booking](actions/get-booking.md) | `GET /bookings/{{id}}` | [docs](https://developer.productive.io/bookings.html) |
| [Get Company](actions/get-company.md) | `GET /companies/{{id}}` | [docs](https://developer.productive.io/companies.html) |
| [Get Contact Entry](actions/get-contact-entry.md) | `GET /contact_entries/{{id}}` | [docs](https://developer.productive.io/contact_entries.html) |
| [Get Contract](actions/get-contract.md) | `GET /contracts/{{id}}` | [docs](https://developer.productive.io/contracts.html) |
| [Get Deal](actions/get-deal.md) | `GET /deals/{{id}}` | [docs](https://developer.productive.io/deals.html) |
| [Get Expense](actions/get-expense.md) | `GET /expenses/{{id}}` | [docs](https://developer.productive.io/expenses.html) |
| [Get Invoice](actions/get-invoice.md) | `GET /invoices/{{id}}` | [docs](https://developer.productive.io/invoices.html) |
| [Get Organization](actions/get-organization.md) | `GET /organizations/{{id}}` | [docs](https://developer.productive.io/organizations.html) |
| [Get Person](actions/get-person.md) | `GET /people/{{id}}` | [docs](https://developer.productive.io/people.html) |
| [Get Project](actions/get-project.md) | `GET /projects/{{id}}` | [docs](https://developer.productive.io/projects.html) |
| [Get Project Assignment](actions/get-project-assignment.md) | `GET /project_assignments/{{id}}` | [docs](https://developer.productive.io/project_assignments.html) |
| [Get Task](actions/get-task.md) | `GET /tasks/{{id}}` | [docs](https://developer.productive.io/tasks.html) |
| [Get Task List](actions/get-task-list.md) | `GET /task_lists/{{id}}` | [docs](https://developer.productive.io/task_lists.html) |
| [Get Team](actions/get-team.md) | `GET /teams/{{id}}` | [docs](https://developer.productive.io/teams.html) |
| [Get Time Entry](actions/get-time-entry.md) | `GET /time_entries/{{id}}` | [docs](https://developer.productive.io/time_entries.html) |
| [Get Timer](actions/get-timer.md) | `GET /timers/{{id}}` | [docs](https://developer.productive.io/timers.html) |
| [Get Timesheet](actions/get-timesheet.md) | `GET /timesheets/{{id}}` | [docs](https://developer.productive.io/timesheets.html) |
| [Get User](actions/get-user.md) | `GET /users/{{id}}` | [docs](https://developer.productive.io/users.html) |
| [Get Workflow](actions/get-workflow.md) | `GET /workflows/{{id}}` | [docs](https://developer.productive.io/workflows.html) |
| [Get Workflow Status](actions/get-workflow-status.md) | `GET /workflow_statuses/{{id}}` | [docs](https://developer.productive.io/workflow_statuses.html) |
| [List Bookings](actions/list-bookings.md) | `GET /bookings` | [docs](https://developer.productive.io/bookings.html) |
| [List Companies](actions/list-companies.md) | `GET /companies` | [docs](https://developer.productive.io/companies.html) |
| [List Contact Entries](actions/list-contact-entries.md) | `GET /contact_entries` | [docs](https://developer.productive.io/contact_entries.html) |
| [List Contracts](actions/list-contracts.md) | `GET /contracts` | [docs](https://developer.productive.io/contracts.html) |
| [List Deals](actions/list-deals.md) | `GET /deals` | [docs](https://developer.productive.io/deals.html) |
| [List Expenses](actions/list-expenses.md) | `GET /expenses` | [docs](https://developer.productive.io/expenses.html) |
| [List Invoices](actions/list-invoices.md) | `GET /invoices` | [docs](https://developer.productive.io/invoices.html) |
| [List Organizations](actions/list-organizations.md) | `GET /organizations` | [docs](https://developer.productive.io/organizations.html) |
| [List People](actions/list-people.md) | `GET /people` | [docs](https://developer.productive.io/people.html) |
| [List Project Assignments](actions/list-project-assignments.md) | `GET /project_assignments` | [docs](https://developer.productive.io/project_assignments.html) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://developer.productive.io/projects.html) |
| [List Task Lists](actions/list-task-lists.md) | `GET /task_lists` | [docs](https://developer.productive.io/task_lists.html) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks` | [docs](https://developer.productive.io/tasks.html) |
| [List Teams](actions/list-teams.md) | `GET /teams` | [docs](https://developer.productive.io/teams.html) |
| [List Time Entries](actions/list-time-entries.md) | `GET /time_entries` | [docs](https://developer.productive.io/time_entries.html) |
| [List Timers](actions/list-timers.md) | `GET /timers` | [docs](https://developer.productive.io/timers.html) |
| [List Timesheets](actions/list-timesheets.md) | `GET /timesheets` | [docs](https://developer.productive.io/timesheets.html) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://developer.productive.io/users.html) |
| [List Workflow Statuses](actions/list-workflow-statuses.md) | `GET /workflow_statuses` | [docs](https://developer.productive.io/workflow_statuses.html) |
| [List Workflows](actions/list-workflows.md) | `GET /workflows` | [docs](https://developer.productive.io/workflows.html) |
