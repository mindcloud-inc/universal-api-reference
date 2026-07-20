# Easy Projects: Native API Reference

A consolidated summary of Easy Projects's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://help.birdviewpsa.com/hc/en-us/articles/115001797351-Birdview-API
- **OpenAPI specification:** https://api.go.easyprojects.net/api/v1
- **API base URL:** `https://api.go.easyprojects.net/api/`

## Authentication

### Birdview OAuth 2.0 Client Credentials

OAuth 2.0 client credentials for Birdview PSA / Easy Projects

### Credentials

- **Birdview User ID:** `userId` · required · Numeric Birdview user ID used to build the client credentials scope user:<id>.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://api.go.easyprojects.net/OAuth2/Authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.go.easyprojects.net/OAuth2/Token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `user:{{credentials.userId}}`.

A machine-to-machine flow is configured.

[Official authentication documentation](https://help.birdviewpsa.com/hc/en-us/articles/9155019022605-OAuth-clients-2-0)

## Pagination

Use `take` in the query string to set the page size (default 100). Use `skip` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `order` in the query string. Use `Name` for ascending order and `NameDesc` for descending order. Only one sort field is accepted.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Task Message](actions/add-task-message.md) | `POST /api/v1/tasks/:id/messages` | [docs](https://api.go.easyprojects.net/api/v1) |
| [Add Time Entry](actions/add-time-entry.md) | `POST /api/v1/tasks/:id/time-entries` | [docs](https://api.go.easyprojects.net/api/v1) |
| [Create Task](actions/create-task.md) | `POST /api/v1/tasks` | [docs](https://api.go.easyprojects.net/api/v1) |
| [Get All Projects](actions/get-all-projects.md) | `GET /api/v1/projects` | [docs](https://api.go.easyprojects.net/api/v1) |
| [Get All Tasks](actions/get-all-tasks.md) | `GET /api/v1/tasks` | [docs](https://api.go.easyprojects.net/api/v1) |
| [Get All Teams](actions/get-all-teams.md) | `GET /api/v1/teams` | [docs](https://api.go.easyprojects.net/api/v1) |
| [Get All Users](actions/get-all-users.md) | `GET /api/v1/users` | [docs](https://api.go.easyprojects.net/api/v1) |
| [Get Current Account](actions/get-current-account.md) | `GET /api/v1/account` | [docs](https://api.go.easyprojects.net/api/v1) |
| [Get Current User](actions/get-current-user.md) | `GET /api/v1/users/current` | [docs](https://api.go.easyprojects.net/api/v1) |
| [Get Customers](actions/get-customers.md) | `GET /api/v1/customers` | [docs](https://api.go.easyprojects.net/api/v1) |
| [Get My Active Tasks](actions/get-my-active-tasks.md) | `GET /api/v1/tasks/my/active` | [docs](https://api.go.easyprojects.net/api/v1) |
| [Get My In Progress Tasks](actions/get-my-in-progress-tasks.md) | `GET /api/v1/tasks/my/in-progress` | [docs](https://api.go.easyprojects.net/api/v1) |
| [Get My Tasks](actions/get-my-tasks.md) | `GET /api/v1/tasks/my` | [docs](https://api.go.easyprojects.net/api/v1) |
| [Get Priorities](actions/get-priorities.md) | `GET /api/v1/priorities` | [docs](https://api.go.easyprojects.net/api/v1) |
| [Get Project](actions/get-project.md) | `GET /api/v1/projects/:id` | [docs](https://api.go.easyprojects.net/api/v1) |
| [Get Project Attachments](actions/get-project-attachments.md) | `GET /api/v1/projects/:id/attachments` | [docs](https://api.go.easyprojects.net/api/v1) |
| [Get Project Kanban](actions/get-project-kanban.md) | `GET /api/v1/projects/:id/kanban` | [docs](https://api.go.easyprojects.net/api/v1) |
| [Get Project Members](actions/get-project-members.md) | `GET /api/v1/projects/:id/members` | [docs](https://api.go.easyprojects.net/api/v1) |
| [Get Project Messages](actions/get-project-messages.md) | `GET /api/v1/projects/:id/messages` | [docs](https://api.go.easyprojects.net/api/v1) |
| [Get Project Statuses](actions/get-project-statuses.md) | `GET /api/v1/project-statuses` | [docs](https://api.go.easyprojects.net/api/v1) |
| [Get Project Tasks](actions/get-project-tasks.md) | `GET /api/v1/projects/:id/tasks` | [docs](https://api.go.easyprojects.net/api/v1) |
| [Get Task](actions/get-task.md) | `GET /api/v1/tasks/:id` | [docs](https://api.go.easyprojects.net/api/v1) |
| [Get Task Attachments](actions/get-task-attachments.md) | `GET /api/v1/tasks/:id/attachments` | [docs](https://api.go.easyprojects.net/api/v1) |
| [Get Task Messages](actions/get-task-messages.md) | `GET /api/v1/tasks/:id/messages` | [docs](https://api.go.easyprojects.net/api/v1) |
| [Get Task Statuses](actions/get-task-statuses.md) | `GET /api/v1/task-statuses` | [docs](https://api.go.easyprojects.net/api/v1) |
| [Get Task Types](actions/get-task-types.md) | `GET /api/v1/task-types` | [docs](https://api.go.easyprojects.net/api/v1) |
| [Get Tasks By Projects](actions/get-tasks-by-projects.md) | `GET /api/v1/tasks/by-projects` | [docs](https://api.go.easyprojects.net/api/v1) |
| [Set Task Assignees](actions/set-task-assignees.md) | `PUT /api/v1/tasks/:id/assignees` | [docs](https://api.go.easyprojects.net/api/v1) |
| [Set Task Done](actions/set-task-done.md) | `PUT /api/v1/tasks/:id/done` | [docs](https://api.go.easyprojects.net/api/v1) |
| [Set Task Status](actions/set-task-status.md) | `PUT /api/v1/tasks/:id/status` | [docs](https://api.go.easyprojects.net/api/v1) |
