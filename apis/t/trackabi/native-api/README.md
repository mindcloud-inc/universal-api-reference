# Trackabi: Native API Reference

A consolidated summary of Trackabi's API configuration and 27 documented operations, with links to official documentation.

- **Official docs:** https://trackabi.com/help/api-docs
- **OpenAPI specification:** https://trackabi.com/dest/swagger.json
- **API base URL:** `https://api.trackabi.com`

## Authentication

### API Key

Use a Trackabi API key for bearer authentication.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://trackabi.com/help/api-docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page_size` in the query string to set the page size (default 30; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `order_by` in the query string. Set the direction separately with `reverse`. Use `0` for ascending order and `1` for descending order. Only one sort field is accepted.

## Endpoints (27 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Assign Project Members](actions/assign-project-members.md) | `POST /api/v1/projects/:projectId/assign-members` | [docs](https://trackabi.com/help/api-docs) |
| [Create Client](actions/create-client.md) | `POST /api/v1/clients` | [docs](https://trackabi.com/help/api-docs) |
| [Create Project](actions/create-project.md) | `POST /api/v1/projects` | [docs](https://trackabi.com/help/api-docs) |
| [Create Task](actions/create-task.md) | `POST /api/v1/projects/:projectId/tasks` | [docs](https://trackabi.com/help/api-docs) |
| [Create Time Entry](actions/create-time-entry.md) | `POST /api/v1/time-entries` | [docs](https://trackabi.com/help/api-docs) |
| [Delete Client](actions/delete-client.md) | `DELETE /api/v1/clients/:clientId` | [docs](https://trackabi.com/help/api-docs) |
| [Delete Project](actions/delete-project.md) | `DELETE /api/v1/projects/:projectId` | [docs](https://trackabi.com/help/api-docs) |
| [Delete Task](actions/delete-task.md) | `DELETE /api/v1/tasks/:taskId` | [docs](https://trackabi.com/help/api-docs) |
| [Delete Time Entry](actions/delete-time-entry.md) | `DELETE /api/v1/time-entry/:timeEntryId` | [docs](https://trackabi.com/help/api-docs) |
| [Get Client](actions/get-client.md) | `GET /api/v1/clients/:clientId` | [docs](https://trackabi.com/help/api-docs) |
| [Get Company Details](actions/get-company-details.md) | `GET /api/v1/company/profile` | [docs](https://trackabi.com/help/api-docs) |
| [Get Project](actions/get-project.md) | `GET /api/v1/projects/:projectId` | [docs](https://trackabi.com/help/api-docs) |
| [Get Task](actions/get-task.md) | `GET /api/v1/tasks/:taskId` | [docs](https://trackabi.com/help/api-docs) |
| [Get Time Entry](actions/get-time-entry.md) | `GET /api/v1/time-entry/:timeEntryId` | [docs](https://trackabi.com/help/api-docs) |
| [List Clients](actions/list-clients.md) | `GET /api/v1/clients` | [docs](https://trackabi.com/help/api-docs) |
| [List Leaves](actions/list-leaves.md) | `GET /api/v1/leaves` | [docs](https://trackabi.com/help/api-docs) |
| [List Members](actions/list-members.md) | `GET /api/v1/members` | [docs](https://trackabi.com/help/api-docs) |
| [List Project Tasks](actions/list-project-tasks.md) | `GET /api/v1/projects/:projectId/tasks` | [docs](https://trackabi.com/help/api-docs) |
| [List Projects](actions/list-projects.md) | `GET /api/v1/projects` | [docs](https://trackabi.com/help/api-docs) |
| [List Task Subtasks](actions/list-task-subtasks.md) | `GET /api/v1/tasks/:taskId/subtasks` | [docs](https://trackabi.com/help/api-docs) |
| [List Tasks](actions/list-tasks.md) | `GET /api/v1/tasks` | [docs](https://trackabi.com/help/api-docs) |
| [List Time Entries](actions/list-time-entries.md) | `GET /api/v1/time-entries` | [docs](https://trackabi.com/help/api-docs) |
| [List Time Types](actions/list-time-types.md) | `GET /api/v1/company/time-types` | [docs](https://trackabi.com/help/api-docs) |
| [Update Client](actions/update-client.md) | `PUT /api/v1/clients/:clientId` | [docs](https://trackabi.com/help/api-docs) |
| [Update Project](actions/update-project.md) | `PUT /api/v1/projects/:projectId` | [docs](https://trackabi.com/help/api-docs) |
| [Update Task](actions/update-task.md) | `PUT /api/v1/tasks/:taskId` | [docs](https://trackabi.com/help/api-docs) |
| [Update Time Entry](actions/update-time-entry.md) | `PUT /api/v1/time-entry/:timeEntryId` | [docs](https://trackabi.com/help/api-docs) |
