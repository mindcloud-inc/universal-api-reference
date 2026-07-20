# Ninety.io: Native API Reference

A consolidated summary of Ninety.io's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://api.public.ninety.io/v1/swagger
- **API base URL:** `https://api.public.ninety.io`

## Authentication

### Personal access token

Authenticate with a Ninety personal access token using the default Bearer authorization header.

### Credentials

- **Personal access token:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.public.ninety.io/v1/swagger)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Issue](actions/create-issue.md) | `POST /v1/issues` | [docs](https://api.public.ninety.io/v1/swagger) |
| [Create Milestone](actions/create-milestone.md) | `POST /v1/milestones` | [docs](https://api.public.ninety.io/v1/swagger) |
| [Create Rock](actions/create-rock.md) | `POST /v1/rocks` | [docs](https://api.public.ninety.io/v1/swagger) |
| [Create To-Do](actions/create-todo.md) | `POST /v1/todos` | [docs](https://api.public.ninety.io/v1/swagger) |
| [Delete Issue](actions/delete-issue.md) | `DELETE /v1/issues/:issueId` | [docs](https://api.public.ninety.io/v1/swagger) |
| [Delete Measurable Note](actions/delete-measurable-note.md) | `DELETE /v1/scorecard/kpis/:kpiId/notes/:periodStartDate` | [docs](https://api.public.ninety.io/v1/swagger) |
| [Delete Measurable Score](actions/delete-measurable-score.md) | `DELETE /v1/scorecard/kpis/:kpiId/scores/:periodStartDate` | [docs](https://api.public.ninety.io/v1/swagger) |
| [Delete Rock](actions/delete-rock.md) | `DELETE /v1/rocks/:id` | [docs](https://api.public.ninety.io/v1/swagger) |
| [Delete To-Do](actions/delete-todo.md) | `DELETE /v1/todos/:id` | [docs](https://api.public.ninety.io/v1/swagger) |
| [Get Issue by Id](actions/get-issue-by-id.md) | `GET /v1/issues/:issueId` | [docs](https://api.public.ninety.io/v1/swagger) |
| [Get Milestone by Id](actions/get-milestone-by-id.md) | `GET /v1/milestones/:id` | [docs](https://api.public.ninety.io/v1/swagger) |
| [Get Rock by Id](actions/get-rock-by-id.md) | `GET /v1/rocks/:id` | [docs](https://api.public.ninety.io/v1/swagger) |
| [Get Teams](actions/get-teams.md) | `GET /v1/teams` | [docs](https://api.public.ninety.io/v1/swagger) |
| [Get To-Do by Id](actions/get-todo-by-id.md) | `GET /v1/todos/:id` | [docs](https://api.public.ninety.io/v1/swagger) |
| [Query Issues](actions/query-issues.md) | `POST /v1/issues/query` | [docs](https://api.public.ninety.io/v1/swagger) |
| [Query Measurables](actions/query-measurables.md) | `POST /v1/scorecard/kpis/query` | [docs](https://api.public.ninety.io/v1/swagger) |
| [Query Rocks](actions/query-rocks.md) | `POST /v1/rocks/query` | [docs](https://api.public.ninety.io/v1/swagger) |
| [Query To-Dos](actions/query-todos.md) | `POST /v1/todos/query` | [docs](https://api.public.ninety.io/v1/swagger) |
| [Update Issue](actions/update-issue.md) | `PATCH /v1/issues/:issueId` | [docs](https://api.public.ninety.io/v1/swagger) |
| [Update Milestone](actions/update-milestone.md) | `PATCH /v1/milestones/:id` | [docs](https://api.public.ninety.io/v1/swagger) |
| [Update Rock](actions/update-rock.md) | `PATCH /v1/rocks/:id` | [docs](https://api.public.ninety.io/v1/swagger) |
| [Update To-Do](actions/update-todo.md) | `PATCH /v1/todos/:id` | [docs](https://api.public.ninety.io/v1/swagger) |
| [Create or Update Measurable Note](actions/upsert-measurable-note.md) | `POST /v1/scorecard/kpis/:kpiId/notes` | [docs](https://api.public.ninety.io/v1/swagger) |
| [Create or Update Measurable Score](actions/upsert-measurable-score.md) | `POST /v1/scorecard/kpis/:kpiId/scores` | [docs](https://api.public.ninety.io/v1/swagger) |
