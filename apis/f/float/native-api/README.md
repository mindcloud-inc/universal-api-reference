# Float: Native API Reference

A consolidated summary of Float's API configuration and 27 documented operations, with links to official documentation.

- **Official docs:** https://developer.float.com/
- **API base URL:** `https://api.float.com/v3`

## Authentication

### API Token

Authenticate with a Float API token and required User-Agent header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.float.com/overview_authentication.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |
| `User-Agent` | `MindCloud Float (apps@mindcloud.co)` |

Responses from this API use JSON.

## Pagination

Use `per-page` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Only one sort field is accepted.

## Endpoints (27 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Allocation](actions/create-allocation.md) | `POST /tasks` | [docs](https://developer.float.com/api_reference.html#Allocations) |
| [Create Client](actions/create-client.md) | `POST /clients` | [docs](https://developer.float.com/api_reference.html#Clients) |
| [Create Logged Time](actions/create-logged-time.md) | `POST /logged-time` | [docs](https://developer.float.com/api_reference.html#Logged_Time) |
| [Create Milestone](actions/create-milestone.md) | `POST /milestones` | [docs](https://developer.float.com/api_reference.html#Milestones) |
| [Create Person](actions/create-person.md) | `POST /people` | [docs](https://developer.float.com/api_reference.html#People) |
| [Create Phase](actions/create-phase.md) | `POST /phases` | [docs](https://developer.float.com/api_reference.html#Phases) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://developer.float.com/api_reference.html#Projects) |
| [Create Project Task](actions/create-project-task.md) | `POST /project-tasks` | [docs](https://developer.float.com/api_reference.html#Project_Tasks) |
| [Create Time Off](actions/create-time-off.md) | `POST /timeoffs` | [docs](https://developer.float.com/api_reference.html#Time_Off) |
| [Get Allocation](actions/get-allocation.md) | `GET /tasks/:task_id` | [docs](https://developer.float.com/api_reference.html#Allocations) |
| [Get People Report](actions/get-people-report.md) | `GET /reports/people` | [docs](https://developer.float.com/api_reference.html#Reports) |
| [Get Person](actions/get-person.md) | `GET /people/:people_id` | [docs](https://developer.float.com/api_reference.html#People) |
| [Get Project](actions/get-project.md) | `GET /projects/:project_id` | [docs](https://developer.float.com/api_reference.html#Projects) |
| [Get Projects Report](actions/get-projects-report.md) | `GET /reports/projects` | [docs](https://developer.float.com/api_reference.html#Reports) |
| [List Allocations](actions/list-allocations.md) | `GET /tasks` | [docs](https://developer.float.com/api_reference.html#Allocations) |
| [List Clients](actions/list-clients.md) | `GET /clients` | [docs](https://developer.float.com/api_reference.html#Clients) |
| [List Logged Time](actions/list-logged-time.md) | `GET /logged-time` | [docs](https://developer.float.com/api_reference.html#Logged_Time) |
| [List Milestones](actions/list-milestones.md) | `GET /milestones` | [docs](https://developer.float.com/api_reference.html#Milestones) |
| [List People](actions/list-people.md) | `GET /people` | [docs](https://developer.float.com/api_reference.html#People) |
| [List Phases](actions/list-phases.md) | `GET /phases` | [docs](https://developer.float.com/api_reference.html#Phases) |
| [List Project Tasks](actions/list-project-tasks.md) | `GET /project-tasks` | [docs](https://developer.float.com/api_reference.html#Project_Tasks) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://developer.float.com/api_reference.html#Projects) |
| [List Roles](actions/list-roles.md) | `GET /roles` | [docs](https://developer.float.com/api_reference.html#Roles) |
| [List Time Off](actions/list-time-off.md) | `GET /timeoffs` | [docs](https://developer.float.com/api_reference.html#Time_Off) |
| [List Time Off Types](actions/list-time-off-types.md) | `GET /timeoff-types` | [docs](https://developer.float.com/api_reference.html#Time_Off_Types) |
| [Update Logged Time](actions/update-logged-time.md) | `PATCH /logged-time/:logged_time_id` | [docs](https://developer.float.com/api_reference.html#Logged_Time) |
| [Update Project](actions/update-project.md) | `PATCH /projects/:project_id` | [docs](https://developer.float.com/api_reference.html#Projects) |
