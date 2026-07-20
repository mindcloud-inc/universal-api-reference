# Manus: Native API Reference

A consolidated summary of Manus's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://open.manus.ai/docs/v1/overview
- **API base URL:** `https://api.manus.ai/v1`

## Authentication

### API Key

Use a Manus API key from API Integration settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://open.manus.ai/docs/quickstart)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–1000). Use `after` in the query string as the pagination cursor.

## Sorting

Set the sort field with `orderBy` in the query string. Set the direction separately with `order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create File](actions/create-file.md) | `POST /files` | [docs](https://open.manus.ai/docs/v1/create-file) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://open.manus.ai/docs/v1/create-project) |
| [Create Task](actions/create-task.md) | `POST /tasks` | [docs](https://open.manus.ai/docs/v1/create-task) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://open.manus.ai/docs/v1/create-webhook) |
| [Delete File](actions/delete-file.md) | `DELETE /files/:file_id` | [docs](https://open.manus.ai/docs/v1/delete-file) |
| [Delete Task](actions/delete-task.md) | `DELETE /tasks/:task_id` | [docs](https://open.manus.ai/docs/v1/delete-task) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/:webhook_id` | [docs](https://open.manus.ai/docs/v1/delete-webhook) |
| [Get File](actions/get-file.md) | `GET /files/:file_id` | [docs](https://open.manus.ai/docs/v1/get-file) |
| [Get Task](actions/get-task.md) | `GET /tasks/:task_id` | [docs](https://open.manus.ai/docs/v1/get-task) |
| [List Files](actions/list-files.md) | `GET /files` | [docs](https://open.manus.ai/docs/v1/list-files) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://open.manus.ai/docs/v1/list-projects) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks` | [docs](https://open.manus.ai/docs/v1/get-tasks) |
| [Update Task](actions/update-task.md) | `PUT /tasks/:task_id` | [docs](https://open.manus.ai/docs/v1/update-task) |
