# Kanban Zone: Native API Reference

A consolidated summary of Kanban Zone's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://docs.kanbanzone.io/apiReference
- **OpenAPI specification:** https://api.swaggerhub.com/apis/kanbanzone/integrations.kanbanzone.io/1.3-oas3/swagger.json
- **API base URL:** `https://integrations.kanbanzone.io/v1`

## Authentication

### API Key

Use a base64-encoded Kanban Zone organization API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://kanbanzone.com/knowledge-base/api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `count` in the query string to set the page size (default 100; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Cards](actions/add-cards.md) | `POST /cards` | [docs](https://docs.kanbanzone.io/apiReference) |
| [Create Card Comment](actions/create-card-comment.md) | `POST /cards/:id/comments` | [docs](https://docs.kanbanzone.io/apiReference) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://docs.kanbanzone.io/apiReference) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/:id` | [docs](https://docs.kanbanzone.io/apiReference) |
| [Get Abandoned Effort Report](actions/get-abandoned-effort-report.md) | `GET /board/:board/reports/abandoned-effort` | [docs](https://docs.kanbanzone.io/apiReference) |
| [Get Allocation Report](actions/get-allocation-report.md) | `GET /board/:board/reports/allocation` | [docs](https://docs.kanbanzone.io/apiReference) |
| [Get Arrival Rate Report](actions/get-arrival-rate-report.md) | `GET /board/:board/reports/arrival-rate` | [docs](https://docs.kanbanzone.io/apiReference) |
| [Get Board](actions/get-board.md) | `GET /board/:board` | [docs](https://docs.kanbanzone.io/apiReference) |
| [Get Card](actions/get-card.md) | `GET /cards/:id` | [docs](https://docs.kanbanzone.io/apiReference) |
| [Get Card Metrics](actions/get-card-metrics.md) | `GET /cards/:id/metrics` | [docs](https://docs.kanbanzone.io/apiReference) |
| [Get Cycle Time Report](actions/get-cycle-time-report.md) | `GET /board/:board/reports/cycle-time` | [docs](https://docs.kanbanzone.io/apiReference) |
| [Get Flow Efficiency Report](actions/get-flow-efficiency-report.md) | `GET /board/:board/reports/flow-efficiency` | [docs](https://docs.kanbanzone.io/apiReference) |
| [Get Flow Report](actions/get-flow-report.md) | `GET /board/:board/reports/flow` | [docs](https://docs.kanbanzone.io/apiReference) |
| [Get Lead Time Report](actions/get-lead-time-report.md) | `GET /board/:board/reports/lead-time` | [docs](https://docs.kanbanzone.io/apiReference) |
| [Get Throughput Report](actions/get-throughput-report.md) | `GET /board/:board/reports/throughput` | [docs](https://docs.kanbanzone.io/apiReference) |
| [Get Webhook Details](actions/get-webhook-details.md) | `GET /webhooks/:id` | [docs](https://docs.kanbanzone.io/apiReference) |
| [List Boards](actions/list-boards.md) | `GET /boards` | [docs](https://docs.kanbanzone.io/apiReference) |
| [List Card Comments](actions/list-card-comments.md) | `GET /cards/:id/comments` | [docs](https://docs.kanbanzone.io/apiReference) |
| [List Cards](actions/list-cards.md) | `GET /cards` | [docs](https://docs.kanbanzone.io/apiReference) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://docs.kanbanzone.io/apiReference) |
| [Move Card](actions/move-card.md) | `POST /cards/:id/move` | [docs](https://docs.kanbanzone.io/apiReference) |
| [Update Card](actions/update-card.md) | `PUT /cards/:id` | [docs](https://docs.kanbanzone.io/apiReference) |
| [Update Webhook](actions/update-webhook.md) | `PUT /webhooks/:id` | [docs](https://docs.kanbanzone.io/apiReference) |
