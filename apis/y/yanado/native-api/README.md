# Yanado: Native API Reference

A consolidated summary of Yanado's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://api.yanado.com/docs/
- **API base URL:** `https://api.yanado.com`

## Authentication

### API Key

Use a Yanado API key generated from Settings > Integrations.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://api.yanado.com/docs/#authentication)

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | `POST /public-api/tasks` | [docs](https://api.yanado.com/docs/#create-task) |
| [Get Task](actions/get-task.md) | `GET /public-api/tasks/:taskId` | [docs](https://api.yanado.com/docs/#get-task) |
| [List Comments](actions/list-comments.md) | `GET /public-api/comments` | [docs](https://api.yanado.com/docs/#get-comments) |
| [List Lists](actions/list-lists.md) | `GET /public-api/lists` | [docs](https://api.yanado.com/docs/#get-lists) |
| [List Notifications](actions/list-notifications.md) | `GET /public-api/notifications/:type` | [docs](https://api.yanado.com/docs/#get-notifications) |
| [List Statuses From List](actions/list-statuses-from-list.md) | `GET /public-api/lists/:listId/statuses` | [docs](https://api.yanado.com/docs/#get-statuses-from-a-list) |
| [List Tasks](actions/list-tasks.md) | `GET /public-api/tasks` | [docs](https://api.yanado.com/docs/#get-tasks) |
| [List Tasks With Emails Attached](actions/list-tasks-with-emails-attached.md) | `GET /public-api/email-tasks` | [docs](https://api.yanado.com/docs/#get-tasks-with-emails-attached) |
| [List Users From List](actions/list-users-from-list.md) | `GET /public-api/lists/:listId/users` | [docs](https://api.yanado.com/docs/#get-users-from-a-list) |
| [List Users From Team](actions/list-users-from-team.md) | `GET /public-api/users` | [docs](https://api.yanado.com/docs/#get-users-from-a-team) |
| [Update Task](actions/update-task.md) | `PUT /public-api/tasks/:taskId` | [docs](https://api.yanado.com/docs/#update-task) |
