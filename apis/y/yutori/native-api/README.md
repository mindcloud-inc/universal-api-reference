# Yutori: Native API Reference

A consolidated summary of Yutori's API configuration and 27 documented operations, with links to official documentation.

- **Official docs:** https://docs.yutori.com
- **OpenAPI specification:** https://docs.yutori.com/openapi.json
- **API base URL:** `https://api.yutori.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.yutori.com/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (27 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Subscribe to Scout](actions/bulk-subscribe-to-scout.md) | `POST /v1/scouting/tasks/:scout_id/subscribe/bulk` | [docs](https://docs.yutori.com/openapi.json) |
| [Create Browsing Task](actions/create-browsing-task.md) | `POST /v1/browsing/tasks` | [docs](https://docs.yutori.com/reference/browsing-create) |
| [Create Chat Completion](actions/create-chat-completion.md) | `POST /v1/chat/completions` | [docs](https://docs.yutori.com/reference/browser-use) |
| [Create Research Task](actions/create-research-task.md) | `POST /v1/research/tasks` | [docs](https://docs.yutori.com/reference/research-create) |
| [Create Scout](actions/create-scout.md) | `POST /v1/scouting/tasks` | [docs](https://docs.yutori.com/reference/scouts-create) |
| [Delete Scout](actions/delete-scout.md) | `DELETE /v1/scouting/tasks/:scout_id` | [docs](https://docs.yutori.com/reference/scouts-delete) |
| [Download Browsing Task Trajectory](actions/download-browsing-task-trajectory.md) | `GET /v1/browsing/tasks/:id/trajectory` | [docs](https://docs.yutori.com/reference/browsing-trajectory) |
| [Get All Scout Updates](actions/get-all-scout-updates.md) | `GET /v1/scouting/updates` | [docs](https://docs.yutori.com/openapi.json) |
| [Get Browsing Task Status](actions/get-browsing-task-status.md) | `GET /v1/browsing/tasks/:id` | [docs](https://docs.yutori.com/reference/browsing-status) |
| [Get Health](actions/get-health.md) | `GET /v1/health` | [docs](https://docs.yutori.com/reference/health) |
| [Get Research Task Result](actions/get-research-task-result.md) | `GET /v1/research/tasks/:task_id` | [docs](https://docs.yutori.com/reference/research-status) |
| [Get Scout](actions/get-scout.md) | `GET /v1/scouting/tasks/:scout_id` | [docs](https://docs.yutori.com/reference/scout-get-detail) |
| [Get Scout Subscriptions](actions/get-scout-subscriptions.md) | `GET /v1/scouting/tasks/:scout_id/subscriptions` | [docs](https://docs.yutori.com/openapi.json) |
| [Get Scout Updates](actions/get-scout-updates.md) | `GET /v1/scouting/tasks/:scout_id/updates` | [docs](https://docs.yutori.com/reference/scouts-updates) |
| [Get Usage](actions/get-usage.md) | `GET /v1/usage` | [docs](https://docs.yutori.com/reference/usage) |
| [List Scouts](actions/list-scouts.md) | `GET /v1/scouting/tasks` | [docs](https://docs.yutori.com/reference/scouts-list) |
| [Mark Scout Complete](actions/mark-scout-complete.md) | `POST /v1/scouting/tasks/:scout_id/complete` | [docs](https://docs.yutori.com/reference/scouts-complete) |
| [Mark Scout Done](actions/mark-scout-done.md) | `POST /v1/scouting/tasks/:scout_id/done` | [docs](https://docs.yutori.com/openapi.json) |
| [Partially Update Scout](actions/partially-update-scout.md) | `PATCH /v1/scouting/tasks/:scout_id` | [docs](https://docs.yutori.com/reference/scouts-patch) |
| [Pause Scout](actions/pause-scout.md) | `POST /v1/scouting/tasks/:scout_id/pause` | [docs](https://docs.yutori.com/openapi.json) |
| [Restart Scout](actions/restart-scout.md) | `POST /v1/scouting/tasks/:scout_id/restart` | [docs](https://docs.yutori.com/reference/scout-restart) |
| [Resume Scout](actions/resume-scout.md) | `POST /v1/scouting/tasks/:scout_id/resume` | [docs](https://docs.yutori.com/openapi.json) |
| [Subscribe to Scout](actions/subscribe-to-scout.md) | `POST /v1/scouting/tasks/:scout_id/subscribe` | [docs](https://docs.yutori.com/openapi.json) |
| [Test Scout Webhook](actions/test-scout-webhook.md) | `POST /v1/scouting/webhooks/test` | [docs](https://docs.yutori.com/reference/webhook) |
| [Unsubscribe from Scout](actions/unsubscribe-from-scout.md) | `POST /v1/scouting/tasks/:scout_id/unsubscribe` | [docs](https://docs.yutori.com/openapi.json) |
| [Update Scout](actions/update-scout.md) | `PUT /v1/scouting/tasks/:scout_id` | [docs](https://docs.yutori.com/openapi.json) |
| [Update Scout Email Settings](actions/update-scout-email-settings.md) | `PUT /v1/scouting/tasks/:scout_id/email-settings` | [docs](https://docs.yutori.com/reference/scouts-email-settings-update) |
