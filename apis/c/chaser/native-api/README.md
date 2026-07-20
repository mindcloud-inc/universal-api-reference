# Chaser: Native API Reference

A consolidated summary of Chaser's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://www.trychaser.com/api
- **API base URL:** `https://slack.chaseforme.com`

## Authentication

### Bearer Token

Use the Chaser webhook token as the bearer token for Chaser API and webhook requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://slack.chaseforme.com/webapi/tasks)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | `POST /webhooks/tasks` | [docs](https://www.trychaser.com/incoming-webhooks) |
| [List Tasks](actions/list-tasks.md) | `GET /webapi/tasks` | [docs](https://www.trychaser.com/api#tasks-list) |
