# Everhour: Native API Reference

A consolidated summary of Everhour's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://everhour.docs.apiary.io/
- **API base URL:** `https://api.everhour.com`

## Authentication

### API Key (Custom)

### Credentials

- **API Key:** `apiKey` · required · Your Everhour API key from My Profile.

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://everhour.docs.apiary.io/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Time](actions/add-time.md) | `POST /time` | [docs](https://everhour.docs.apiary.io/) |
| [Archive or Unarchive Project](actions/archive-or-unarchive-project.md) | `PATCH /projects/:projectId/archive` | [docs](https://everhour.docs.apiary.io/) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://everhour.docs.apiary.io/) |
| [Create Task](actions/create-task.md) | `POST /projects/:projectId/tasks` | [docs](https://everhour.docs.apiary.io/) |
| [Delete Task](actions/delete-task.md) | `DELETE /tasks/:taskId` | [docs](https://everhour.docs.apiary.io/) |
| [Delete Time Record](actions/delete-time-record.md) | `DELETE /time/:timeId` | [docs](https://everhour.docs.apiary.io/) |
| [Get Current User](actions/get-current-user.md) | `GET /users/me` | [docs](https://everhour.docs.apiary.io/reference/0/users/your-profile) |
| [Get Project](actions/get-project.md) | `GET /projects/:projectId` | [docs](https://everhour.docs.apiary.io/) |
| [Get Running Timer](actions/get-running-timer.md) | `GET /timers/current` | [docs](https://everhour.docs.apiary.io/) |
| [Get Task](actions/get-task.md) | `GET /tasks/:taskId` | [docs](https://everhour.docs.apiary.io/) |
| [List Project Tasks](actions/list-project-tasks.md) | `GET /projects/:projectId/tasks` | [docs](https://everhour.docs.apiary.io/) |
| [List Project Time Records](actions/list-project-time-records.md) | `GET /projects/:projectId/time` | [docs](https://everhour.docs.apiary.io/) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://everhour.docs.apiary.io/) |
| [List Task Time Records](actions/list-task-time-records.md) | `GET /tasks/:taskId/time` | [docs](https://everhour.docs.apiary.io/) |
| [List Time Records](actions/list-time-records.md) | `GET /team/time` | [docs](https://everhour.docs.apiary.io/) |
| [List User Time Records](actions/list-user-time-records.md) | `GET /users/:userId/time` | [docs](https://everhour.docs.apiary.io/) |
| [List Users](actions/list-users.md) | `GET /team/users` | [docs](https://everhour.docs.apiary.io/) |
| [Search Project Tasks](actions/search-project-tasks.md) | `GET /projects/:projectId/tasks/search` | [docs](https://everhour.docs.apiary.io/) |
| [Search Tasks](actions/search-tasks.md) | `GET /tasks/search` | [docs](https://everhour.docs.apiary.io/) |
| [Start Timer](actions/start-timer.md) | `POST /timers` | [docs](https://everhour.docs.apiary.io/) |
| [Stop Timer](actions/stop-timer.md) | `DELETE /timers/current` | [docs](https://everhour.docs.apiary.io/) |
| [Update Project](actions/update-project.md) | `PUT /projects/:projectId` | [docs](https://everhour.docs.apiary.io/) |
| [Update Task](actions/update-task.md) | `PUT /tasks/:taskId` | [docs](https://everhour.docs.apiary.io/) |
| [Update Time Record](actions/update-time-record.md) | `PUT /time/:timeId` | [docs](https://everhour.docs.apiary.io/) |
