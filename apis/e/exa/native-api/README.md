# Exa: Native API Reference

A consolidated summary of Exa's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://exa.ai/docs/reference/search-api-guide
- **OpenAPI specification:** https://exa.ai/docs/reference/openapi-spec
- **API base URL:** `https://api.exa.ai`

## Authentication

### API Key

Authenticate Exa with an API key. Exa accepts API keys in the x-api-key header and, per its OpenAPI spec, as a Bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://exa.ai/docs/reference/search)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

The next-page cursor is read from `nextCursor`.

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–100). Use `cursor` in the query string as the pagination cursor.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Answer](actions/answer.md) | `POST /answer` | [docs](https://exa.ai/docs/reference/answer) |
| [Cancel Webset](actions/cancel-webset.md) | `POST /websets/v0/websets/:id/cancel` | [docs](https://exa.ai/docs/websets/api/websets/cancel-a-running-webset) |
| [Cancel Webset Enrichment](actions/cancel-webset-enrichment.md) | `POST /websets/v0/websets/:webset/enrichments/:id/cancel` | [docs](https://exa.ai/docs/websets/api/websets/enrichments/cancel-a-running-enrichment) |
| [Cancel Webset Search](actions/cancel-webset-search.md) | `POST /websets/v0/websets/:webset/searches/:id/cancel` | [docs](https://exa.ai/docs/websets/api/websets/searches/cancel-a-running-search) |
| [Context](actions/context.md) | `POST /context` | [docs](https://exa.ai/docs/reference/context) |
| [Create Import](actions/create-import.md) | `POST /websets/v0/imports` | [docs](https://exa.ai/docs/websets/api/imports/create-an-import) |
| [Create Monitor](actions/create-monitor.md) | `POST /monitors` | [docs](https://exa.ai/docs/websets/api/monitors/create-a-monitor) |
| [Create Webhook](actions/create-webhook.md) | `POST /websets/v0/webhooks` | [docs](https://exa.ai/docs/websets/api/webhooks/create-a-webhook) |
| [Create Webset](actions/create-webset.md) | `POST /websets/v0/websets` | [docs](https://exa.ai/docs/websets/api/websets/create-a-webset) |
| [Create Webset Enrichment](actions/create-webset-enrichment.md) | `POST /websets/v0/websets/:webset/enrichments` | [docs](https://exa.ai/docs/websets/api/websets/enrichments/create-an-enrichment) |
| [Create Webset Search](actions/create-webset-search.md) | `POST /websets/v0/websets/:webset/searches` | [docs](https://exa.ai/docs/websets/api/websets/searches/create-a-search) |
| [Delete Monitor](actions/delete-monitor.md) | `DELETE /monitors/:id` | [docs](https://exa.ai/docs/websets/api/monitors/delete-monitor) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /websets/v0/webhooks/:id` | [docs](https://exa.ai/docs/websets/api/webhooks/delete-a-webhook) |
| [Delete Webset](actions/delete-webset.md) | `DELETE /websets/v0/websets/:id` | [docs](https://exa.ai/docs/websets/api/websets/delete-a-webset) |
| [Delete Webset Enrichment](actions/delete-webset-enrichment.md) | `DELETE /websets/v0/websets/:webset/enrichments/:id` | [docs](https://exa.ai/docs/websets/api/websets/enrichments/delete-an-enrichment) |
| [Find Similar Links](actions/find-similar-links.md) | `POST /findSimilar` | [docs](https://exa.ai/docs/reference/find-similar-links) |
| [Get Contents](actions/get-contents.md) | `POST /contents` | [docs](https://exa.ai/docs/reference/get-contents) |
| [Get Event](actions/get-event.md) | `GET /websets/v0/events/:id` | [docs](https://exa.ai/docs/websets/api/events/get-an-event) |
| [Get Import](actions/get-import.md) | `GET /websets/v0/imports/:id` | [docs](https://exa.ai/docs/websets/api/imports/get-import) |
| [Get Monitor](actions/get-monitor.md) | `GET /monitors/:id` | [docs](https://exa.ai/docs/websets/api/monitors/get-monitor) |
| [Get Monitor Run](actions/get-monitor-run.md) | `GET /monitors/:id/runs/:runId` | [docs](https://exa.ai/docs/websets/api/monitors/runs/get-monitor-run) |
| [Get Webhook](actions/get-webhook.md) | `GET /websets/v0/webhooks/:id` | [docs](https://exa.ai/docs/websets/api/webhooks/get-a-webhook) |
| [Get Webset](actions/get-webset.md) | `GET /websets/v0/websets/:id` | [docs](https://exa.ai/docs/websets/api/websets/get-a-webset) |
| [Get Webset Enrichment](actions/get-webset-enrichment.md) | `GET /websets/v0/websets/:webset/enrichments/:id` | [docs](https://exa.ai/docs/websets/api/websets/enrichments/get-an-enrichment) |
| [Get Webset Item](actions/get-webset-item.md) | `GET /websets/v0/websets/:webset/items/:id` | [docs](https://exa.ai/docs/websets/api/websets/items/get-an-item) |
| [Get Webset Search](actions/get-webset-search.md) | `GET /websets/v0/websets/:webset/searches/:id` | [docs](https://exa.ai/docs/websets/api/websets/searches/get-a-search) |
| [List Events](actions/list-events.md) | `GET /websets/v0/events` | [docs](https://exa.ai/docs/websets/api/events/list-all-events) |
| [List Imports](actions/list-imports.md) | `GET /websets/v0/imports` | [docs](https://exa.ai/docs/websets/api/imports/list-imports) |
| [List Monitor Runs](actions/list-monitor-runs.md) | `GET /monitors/:id/runs` | [docs](https://exa.ai/docs/websets/api/monitors/runs/list-monitor-runs) |
| [List Monitors](actions/list-monitors.md) | `GET /monitors` | [docs](https://exa.ai/docs/websets/api/monitors/list-monitors) |
| [List Webhooks](actions/list-webhooks.md) | `GET /websets/v0/webhooks` | [docs](https://exa.ai/docs/websets/api/webhooks/list-webhooks) |
| [List Webset Items](actions/list-webset-items.md) | `GET /websets/v0/websets/:webset/items` | [docs](https://exa.ai/docs/websets/api/websets/items/list-all-items-for-a-webset) |
| [List Websets](actions/list-websets.md) | `GET /websets/v0/websets` | [docs](https://exa.ai/docs/websets/api/websets/list-all-websets) |
| [Preview Webset](actions/preview-webset.md) | `POST /websets/v0/websets/preview` | [docs](https://exa.ai/docs/websets/api/websets/preview-a-webset) |
| [Search](actions/search.md) | `POST /search` | [docs](https://exa.ai/docs/reference/search) |
| [Trigger Monitor Run](actions/trigger-monitor-run.md) | `POST /monitors/:id/trigger` | [docs](https://exa.ai/docs/reference/monitors-api-guide-for-coding-agents#post-/monitors/id/trigger-%E2%80%94-trigger-a-run) |
| [Update Monitor](actions/update-monitor.md) | `PATCH /monitors/:id` | [docs](https://exa.ai/docs/websets/api/monitors/update-monitor) |
| [Update Webhook](actions/update-webhook.md) | `PATCH /websets/v0/webhooks/:id` | [docs](https://exa.ai/docs/websets/api/webhooks/update-a-webhook) |
| [Update Webset](actions/update-webset.md) | `POST /websets/v0/websets/:id` | [docs](https://exa.ai/docs/websets/api/websets/update-a-webset) |
| [Update Webset Enrichment](actions/update-webset-enrichment.md) | `PATCH /websets/v0/websets/:webset/enrichments/:id` | [docs](https://exa.ai/docs/websets/api/websets/enrichments/update-an-enrichment) |
