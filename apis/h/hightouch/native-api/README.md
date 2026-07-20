# Hightouch: Native API Reference

A consolidated summary of Hightouch's API configuration and 36 documented operations, with links to official documentation.

- **Official docs:** https://hightouch.com/docs/developer-tools/api-guide
- **OpenAPI specification:** https://api.hightouch.io/api/swagger.json
- **API base URL:** `https://api.hightouch.com/api/v1`

## Authentication

### API Key

Use a Hightouch workspace API key created by an Admin user.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://hightouch.com/docs/developer-tools/api-guide)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `orderBy` in the query string. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (36 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Decision Engine Message](actions/create-decision-engine-message.md) | `POST /decision-engine/flow/{flowId}/messages` | [docs](https://api.hightouch.io/api/swagger.json) |
| [Create Destination](actions/create-destination.md) | `POST /destinations` | [docs](https://api.hightouch.io/api/swagger.json) |
| [Create Event Contract](actions/create-event-contract.md) | `POST /events/contracts` | [docs](https://api.hightouch.io/api/swagger.json) |
| [Create Model](actions/create-model.md) | `POST /models` | [docs](https://api.hightouch.io/api/swagger.json) |
| [Create Source](actions/create-source.md) | `POST /sources` | [docs](https://api.hightouch.io/api/swagger.json) |
| [Create Sync](actions/create-sync.md) | `POST /syncs` | [docs](https://api.hightouch.io/api/swagger.json) |
| [Get Decision Engine Flow](actions/get-decision-engine-flow.md) | `GET /decision-engine/flow/{flowId}` | [docs](https://api.hightouch.io/api/swagger.json) |
| [Get Decision Engine Message](actions/get-decision-engine-message.md) | `GET /decision-engine/flow/{flowId}/messages/{messageId}` | [docs](https://api.hightouch.io/api/swagger.json) |
| [Get Destination](actions/get-destination.md) | `GET /destinations/{destinationId}` | [docs](https://api.hightouch.io/api/swagger.json) |
| [Get Event Contract](actions/get-event-contract.md) | `GET /events/contracts/{contractId}` | [docs](https://api.hightouch.io/api/swagger.json) |
| [Get IDR Reprocess Status](actions/get-idr-reprocess-status.md) | `GET /idr/{graphId}/reprocess-status/{requestId}` | [docs](https://api.hightouch.io/api/swagger.json) |
| [Get Model](actions/get-model.md) | `GET /models/{modelId}` | [docs](https://api.hightouch.io/api/swagger.json) |
| [Get Source](actions/get-source.md) | `GET /sources/{sourceId}` | [docs](https://api.hightouch.io/api/swagger.json) |
| [Get Sync](actions/get-sync.md) | `GET /syncs/{syncId}` | [docs](https://api.hightouch.io/api/swagger.json) |
| [Get Sync Sequence Run](actions/get-sync-sequence-run.md) | `GET /sync-sequences/runs/{syncSequenceRunId}` | [docs](https://api.hightouch.io/api/swagger.json) |
| [List Decision Engine Flows](actions/list-decision-engine-flows.md) | `GET /decision-engine/flows` | [docs](https://api.hightouch.io/api/swagger.json) |
| [List Decision Engine Messages](actions/list-decision-engine-messages.md) | `GET /decision-engine/flow/{flowId}/messages` | [docs](https://api.hightouch.io/api/swagger.json) |
| [List Destinations](actions/list-destinations.md) | `GET /destinations` | [docs](https://api.hightouch.io/api/swagger.json) |
| [List Event Contracts](actions/list-event-contracts.md) | `GET /events/contracts` | [docs](https://api.hightouch.io/api/swagger.json) |
| [List IDR Runs](actions/list-idr-runs.md) | `GET /idr/{graphId}/runs` | [docs](https://api.hightouch.io/api/swagger.json) |
| [List Models](actions/list-models.md) | `GET /models` | [docs](https://api.hightouch.io/api/swagger.json) |
| [List Sources](actions/list-sources.md) | `GET /sources` | [docs](https://api.hightouch.io/api/swagger.json) |
| [List Sync Runs](actions/list-sync-runs.md) | `GET /syncs/{syncId}/runs` | [docs](https://api.hightouch.io/api/swagger.json) |
| [List Syncs](actions/list-syncs.md) | `GET /syncs` | [docs](https://api.hightouch.io/api/swagger.json) |
| [Queue IDR Identifiers For Reprocessing](actions/queue-idr-identifiers-for-reprocessing.md) | `POST /idr/{graphId}/queue-for-reprocessing` | [docs](https://api.hightouch.io/api/swagger.json) |
| [Trigger Decision Engine Flow Run](actions/trigger-decision-engine-flow-run.md) | `POST /decision-engine/flow/{flowId}/run` | [docs](https://api.hightouch.io/api/swagger.json) |
| [Trigger IDR Run](actions/trigger-idr-run.md) | `POST /idr/{graphId}/trigger` | [docs](https://api.hightouch.io/api/swagger.json) |
| [Trigger Sync](actions/trigger-sync.md) | `POST /syncs/{syncId}/trigger` | [docs](https://api.hightouch.io/api/swagger.json) |
| [Trigger Sync From ID or Slug](actions/trigger-sync-from-id-or-slug.md) | `POST /syncs/trigger` | [docs](https://api.hightouch.io/api/swagger.json) |
| [Trigger Sync Sequence](actions/trigger-sync-sequence.md) | `POST /sync-sequences/{syncSequenceId}/trigger` | [docs](https://api.hightouch.io/api/swagger.json) |
| [Update Decision Engine Message](actions/update-decision-engine-message.md) | `PATCH /decision-engine/flow/{flowId}/messages/{messageId}` | [docs](https://api.hightouch.io/api/swagger.json) |
| [Update Destination](actions/update-destination.md) | `PATCH /destinations/{destinationId}` | [docs](https://api.hightouch.io/api/swagger.json) |
| [Update Event Contract](actions/update-event-contract.md) | `PATCH /events/contracts/{contractId}` | [docs](https://api.hightouch.io/api/swagger.json) |
| [Update Model](actions/update-model.md) | `PATCH /models/{modelId}` | [docs](https://api.hightouch.io/api/swagger.json) |
| [Update Source](actions/update-source.md) | `PATCH /sources/{sourceId}` | [docs](https://api.hightouch.io/api/swagger.json) |
| [Update Sync](actions/update-sync.md) | `PATCH /syncs/{syncId}` | [docs](https://api.hightouch.io/api/swagger.json) |
