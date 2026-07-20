# TickTick: Native API Reference

A consolidated summary of TickTick's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://developer.ticktick.com/docs/index.html#/openapi
- **API base URL:** `https://api.ticktick.com`

## Authentication

### OAuth 2.0

OAuth 2.0 Authorization Code flow for TickTick Open API.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://ticktick.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://ticktick.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `tasks:write tasks:read`.

[Official authentication documentation](https://developer.ticktick.com/docs/openapi.md)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Complete Task](actions/complete-task.md) | `POST /open/v1/project/:projectId/task/:taskId/complete` | [docs](https://developer.ticktick.com/docs/index.html#/openapi?id=complete-task) |
| [Create Project](actions/create-project.md) | `POST /open/v1/project` | [docs](https://developer.ticktick.com/docs/index.html#/openapi?id=create-project) |
| [Create Task](actions/create-task.md) | `POST /open/v1/task` | [docs](https://developer.ticktick.com/docs/index.html#/openapi?id=create-task) |
| [Delete Project](actions/delete-project.md) | `DELETE /open/v1/project/:projectId` | [docs](https://developer.ticktick.com/docs/index.html#/openapi?id=delete-project) |
| [Delete Task](actions/delete-task.md) | `DELETE /open/v1/project/:projectId/task/:taskId` | [docs](https://developer.ticktick.com/docs/index.html#/openapi?id=delete-task) |
| [Get Project By ID](actions/get-project-by-id.md) | `GET /open/v1/project/:projectId` | [docs](https://developer.ticktick.com/docs/index.html#/openapi?id=get-project-by-id) |
| [Get Project With Data](actions/get-project-with-data.md) | `GET /open/v1/project/:projectId/data` | [docs](https://developer.ticktick.com/docs/index.html#/openapi?id=get-project-with-data) |
| [Get Task](actions/get-task.md) | `GET /open/v1/project/:projectId/task/:taskId` | [docs](https://developer.ticktick.com/docs/index.html#/openapi?id=get-task-by-project-id-and-task-id) |
| [List User Projects](actions/list-user-projects.md) | `GET /open/v1/project` | [docs](https://developer.ticktick.com/docs/index.html#/openapi?id=get-user-project) |
| [Update Project](actions/update-project.md) | `POST /open/v1/project/:projectId` | [docs](https://developer.ticktick.com/docs/index.html#/openapi?id=update-project) |
| [Update Task](actions/update-task.md) | `POST /open/v1/task/:taskId` | [docs](https://developer.ticktick.com/docs/index.html#/openapi?id=update-task) |
