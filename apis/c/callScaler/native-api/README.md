# CallScaler: Native API Reference

A consolidated summary of CallScaler's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://callscaler.com/docs/api-reference
- **API base URL:** `https://callscaler.com/api/v1`

## Authentication

### API Key

Use a CallScaler API key. Send it as a Bearer token in the Authorization header on every request.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://callscaler.com/docs/api-reference)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–500). Use `offset` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `sort_by` in the query string. Set the direction separately with `sort_order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429`. Wait 12 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Number Group Members](actions/add-number-group-members.md) | `POST /number-groups/:id/members` | [docs](https://callscaler.com/docs/api-resources) |
| [Batch Lookup Calls](actions/batch-lookup-calls.md) | `POST /calls/batch` | [docs](https://callscaler.com/docs/api-calls) |
| [Create Call Flow](actions/create-call-flow.md) | `POST /call-flows` | [docs](https://callscaler.com/docs/api-resources) |
| [Create Number Group](actions/create-number-group.md) | `POST /number-groups` | [docs](https://callscaler.com/docs/api-resources) |
| [Create Number Pool](actions/create-number-pool.md) | `POST /number-pools` | [docs](https://callscaler.com/docs/api-resources) |
| [Delete Call Flow](actions/delete-call-flow.md) | `DELETE /call-flows/:id` | [docs](https://callscaler.com/docs/api-resources) |
| [Delete Number Group](actions/delete-number-group.md) | `DELETE /number-groups/:id` | [docs](https://callscaler.com/docs/api-resources) |
| [Download Call Recording](actions/download-call-recording.md) | `GET /calls/:id/recording` | [docs](https://callscaler.com/docs/api-calls) |
| [Export Calls CSV](actions/export-calls-csv.md) | `GET /calls/export` | [docs](https://callscaler.com/docs/api-calls) |
| [Get Call](actions/get-call.md) | `GET /calls/:id` | [docs](https://callscaler.com/docs/api-calls) |
| [Get Call Analytics](actions/get-call-analytics.md) | `GET /analytics/calls` | [docs](https://callscaler.com/docs/api-analytics) |
| [Get Call Flow](actions/get-call-flow.md) | `GET /call-flows/:id` | [docs](https://callscaler.com/docs/api-resources) |
| [Get Call Transcription](actions/get-call-transcription.md) | `GET /calls/:id/transcription` | [docs](https://callscaler.com/docs/api-calls) |
| [Get Number](actions/get-number.md) | `GET /numbers/:id` | [docs](https://callscaler.com/docs/api-resources) |
| [Get Number Group Bulk Stats](actions/get-number-group-bulk-stats.md) | `GET /number-groups/bulk-stats` | [docs](https://callscaler.com/docs/api-resources) |
| [Get Number Pool](actions/get-number-pool.md) | `GET /number-pools/:id` | [docs](https://callscaler.com/docs/api-resources) |
| [List Call Flow Versions](actions/list-call-flow-versions.md) | `GET /call-flows/:id/versions` | [docs](https://callscaler.com/docs/api-resources) |
| [List Call Flows](actions/list-call-flows.md) | `GET /call-flows` | [docs](https://callscaler.com/docs/api-resources) |
| [List Calls](actions/list-calls.md) | `GET /calls` | [docs](https://callscaler.com/docs/api-calls) |
| [List Number Group Members](actions/list-number-group-members.md) | `GET /number-groups/:id/members` | [docs](https://callscaler.com/docs/api-resources) |
| [List Number Groups](actions/list-number-groups.md) | `GET /number-groups` | [docs](https://callscaler.com/docs/api-resources) |
| [List Number Pools](actions/list-number-pools.md) | `GET /number-pools` | [docs](https://callscaler.com/docs/api-resources) |
| [List Numbers](actions/list-numbers.md) | `GET /numbers` | [docs](https://callscaler.com/docs/api-resources) |
| [Purchase Number](actions/purchase-number.md) | `POST /numbers/purchase` | [docs](https://callscaler.com/docs/api-resources) |
| [Release Number](actions/release-number.md) | `DELETE /numbers/:id` | [docs](https://callscaler.com/docs/api-resources) |
| [Remove Number Group Member](actions/remove-number-group-member.md) | `DELETE /number-groups/:id/members/:numId` | [docs](https://callscaler.com/docs/api-resources) |
| [Search Available Numbers](actions/search-available-numbers.md) | `POST /numbers/search` | [docs](https://callscaler.com/docs/api-resources) |
| [Update Call Flow](actions/update-call-flow.md) | `PUT /call-flows/:id` | [docs](https://callscaler.com/docs/api-resources) |
| [Update Number](actions/update-number.md) | `PATCH /numbers/:id` | [docs](https://callscaler.com/docs/api-resources) |
| [Update Number Group](actions/update-number-group.md) | `PUT /number-groups/:id` | [docs](https://callscaler.com/docs/api-resources) |
