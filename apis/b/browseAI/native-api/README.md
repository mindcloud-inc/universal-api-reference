# Browse AI: Native API Reference

A consolidated summary of Browse AI's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://developers.browse.ai/v2
- **OpenAPI specification:** https://api.browse.ai/v2/openapi
- **API base URL:** `https://api.browse.ai/v2`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.browse.ai/en/articles/12683249-api-guide-getting-started#h_5304b03498)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `pageSize` in the query string to set the page size (default 10; accepted range 1–10). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Multiple sort fields can be combined.

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check System Status](actions/check-system-status.md) | `GET /status` | [docs](https://developers.browse.ai/v2#tag/system/GET/status) |
| [Create Monitor](actions/create-monitor.md) | `POST /robots/:robotId/monitors` | [docs](https://developers.browse.ai/v2#tag/monitors) |
| [Create Webhook](actions/create-webhook.md) | `POST /robots/:robotId/webhooks` | [docs](https://developers.browse.ai/v2#webhooks) |
| [Delete Monitor](actions/delete-monitor.md) | `DELETE /robots/:robotId/monitors/:monitorId` | [docs](https://developers.browse.ai/v2#tag/monitors) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /robots/:robotId/webhooks/:webhookId` | [docs](https://developers.browse.ai/v2#webhooks) |
| [Get Bulk Run](actions/get-bulk-run.md) | `GET /robots/:robotId/bulk-runs/:bulkRunId` | [docs](https://developers.browse.ai/v2#tag/bulk-runs) |
| [Get Monitor](actions/get-monitor.md) | `GET /robots/:robotId/monitors/:monitorId` | [docs](https://developers.browse.ai/v2#tag/monitors) |
| [Get Robot](actions/get-robot.md) | `GET /robots/:robotId` | [docs](https://developers.browse.ai/v2#tag/robots/GET/robots/{robotId}) |
| [Get Robot Task](actions/get-robot-task.md) | `GET /robots/:robotId/tasks/:taskId` | [docs](https://developers.browse.ai/v2#tag/tasks) |
| [List Bulk Runs](actions/list-bulk-runs.md) | `GET /robots/:robotId/bulk-runs` | [docs](https://developers.browse.ai/v2#tag/bulk-runs) |
| [List Monitors](actions/list-monitors.md) | `GET /robots/:robotId/monitors` | [docs](https://developers.browse.ai/v2#tag/monitors) |
| [List Robot Tasks](actions/list-robot-tasks.md) | `GET /robots/:robotId/tasks` | [docs](https://developers.browse.ai/v2#tag/tasks) |
| [List Robots](actions/list-robots.md) | `GET /robots` | [docs](https://developers.browse.ai/v2#tag/robots/GET/robots) |
| [List Teams](actions/list-teams.md) | `GET /teams` |  |
| [List Webhooks](actions/list-webhooks.md) | `GET /robots/:robotId/webhooks` | [docs](https://developers.browse.ai/v2#webhooks) |
| [Run Robot Task](actions/run-robot-task.md) | `POST /robots/:robotId/tasks` | [docs](https://developers.browse.ai/v2#tag/tasks) |
| [Start Bulk Run](actions/start-bulk-run.md) | `POST /robots/:robotId/bulk-runs` | [docs](https://developers.browse.ai/v2#tag/bulk-runs) |
| [Update Monitor](actions/update-monitor.md) | `PATCH /robots/:robotId/monitors/:monitorId` | [docs](https://developers.browse.ai/v2#tag/monitors) |
| [Update Robot Cookies](actions/update-robot-cookies.md) | `PATCH /robots/:robotId/cookies` | [docs](https://developers.browse.ai/v2#tag/robots/PATCH/robots/{robotId}/cookies) |
