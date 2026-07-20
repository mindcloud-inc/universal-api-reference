# Worktivity: Native API Reference

A consolidated summary of Worktivity's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://useworktivity.com/for-developers
- **OpenAPI specification:** https://open-api.useworktivity.com/swagger/v1.0/swagger.json
- **API base URL:** `https://open-api.useworktivity.com`

## Authentication

### API Key

Authenticate Worktivity Open API requests with an API key supplied as the `x_api_key` query parameter.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://useworktivity.com/for-developers)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `data.pageCount`.

## Pagination

Use `PageSize` in the request body to set the page size (default 50; accepted range 1–100). Use `Page` in the request body to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Block or Unblock Employee](actions/block-or-unblock-employee.md) | `POST /Employee/Block` | [docs](https://useworktivity.com/for-developers) |
| [Create Employee](actions/create-employee.md) | `POST /Employee/Create` | [docs](https://useworktivity.com/for-developers) |
| [Create or Update Customer](actions/create-or-update-customer.md) | `POST /Project/AddUpdateCustomer` | [docs](https://useworktivity.com/for-developers) |
| [Create or Update Project](actions/create-or-update-project.md) | `POST /Project/AddUpdateProject` | [docs](https://useworktivity.com/for-developers) |
| [Create or Update Project Task](actions/create-or-update-project-task.md) | `POST /Project/AddUpdateTask` | [docs](https://useworktivity.com/for-developers) |
| [Create or Update Team](actions/create-or-update-team.md) | `POST /Team/AddOrUpdate` | [docs](https://useworktivity.com/for-developers) |
| [Get Application Usage Summary](actions/get-application-usage-summary.md) | `POST /Insights/AppsSummary` | [docs](https://useworktivity.com/for-developers) |
| [Get Productivity Insights](actions/get-productivity-insights.md) | `POST /Insights/Productivity` | [docs](https://useworktivity.com/for-developers) |
| [Get Project](actions/get-project.md) | `POST /Project/Get` | [docs](https://useworktivity.com/for-developers) |
| [Get Project Task](actions/get-project-task.md) | `POST /Project/GetTask` | [docs](https://useworktivity.com/for-developers) |
| [Get Work Times Analytics](actions/get-work-times-analytics.md) | `POST /Insights/WorkTimes` | [docs](https://useworktivity.com/for-developers) |
| [List Customers](actions/list-customers.md) | `POST /Project/ListCustomers` | [docs](https://useworktivity.com/for-developers) |
| [List Employees](actions/list-employees.md) | `POST /Employee/List` | [docs](https://useworktivity.com/for-developers) |
| [List Manual Time Entries](actions/list-manual-time-entries.md) | `POST /TimeEntry/List` | [docs](https://useworktivity.com/for-developers) |
| [List Project Task Comments](actions/list-project-task-comments.md) | `POST /Project/ListComments` | [docs](https://useworktivity.com/for-developers) |
| [List Project Tasks](actions/list-project-tasks.md) | `POST /Project/ListTasks` | [docs](https://useworktivity.com/for-developers) |
| [List Projects](actions/list-projects.md) | `POST /Project/List` | [docs](https://useworktivity.com/for-developers) |
| [List Screenshots](actions/list-screenshots.md) | `POST /Screenshots/List` | [docs](https://useworktivity.com/for-developers) |
| [List System Enumerations](actions/list-system-enumerations.md) | `GET /Definition/ListEnums` | [docs](https://useworktivity.com/for-developers) |
| [List Teams](actions/list-teams.md) | `POST /Team/List` | [docs](https://useworktivity.com/for-developers) |
| [List Timesheets](actions/list-timesheets.md) | `POST /Timesheet/List` | [docs](https://useworktivity.com/for-developers) |
| [Update Employee](actions/update-employee.md) | `POST /Employee/Update` | [docs](https://useworktivity.com/for-developers) |
| [Update Project Task Assignees](actions/update-project-task-assignees.md) | `POST /Project/UpdateTaskAssignees` | [docs](https://useworktivity.com/for-developers) |
| [Update Project Task Status](actions/update-project-task-status.md) | `POST /Project/UpdateTaskStatus` | [docs](https://useworktivity.com/for-developers) |
