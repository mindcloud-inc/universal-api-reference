# Allscreenshots: Native API Reference

A consolidated summary of Allscreenshots's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://docs.allscreenshots.com
- **API base URL:** `https://api.allscreenshots.com`

## Authentication

### API Key

Connect with an Allscreenshots API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.allscreenshots.com/getting-started/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 20). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Async Screenshot Job](actions/create-async-screenshot-job.md) | `POST /v1/screenshots/async` | [docs](https://docs.allscreenshots.com/api-reference/async-jobs) |
| [Create Bulk Job](actions/create-bulk-job.md) | `POST /v1/screenshots/bulk` | [docs](https://docs.allscreenshots.com/api-reference/bulk) |
| [Create Composition](actions/create-composition.md) | `POST /v1/screenshots/compose` | [docs](https://docs.allscreenshots.com/api-reference/compose) |
| [Create Screenshot](actions/create-screenshot.md) | `POST /v1/screenshots` | [docs](https://docs.allscreenshots.com/api-reference/screenshots) |
| [Get Bulk Job Status](actions/get-bulk-job-status.md) | `GET /v1/screenshots/bulk/:bulkJobId` | [docs](https://docs.allscreenshots.com/api-reference/bulk) |
| [Get Screenshot Job Output Result](actions/get-screenshot-job-output-result.md) | `GET /v1/screenshots/jobs/:jobId/result/:outputId` | [docs](https://docs.allscreenshots.com/api-reference/outputs) |
| [Get Screenshot Job Result](actions/get-screenshot-job-result.md) | `GET /v1/screenshots/jobs/:jobId/result` | [docs](https://docs.allscreenshots.com/api-reference/async-jobs) |
| [Get Screenshot Job Status](actions/get-screenshot-job-status.md) | `GET /v1/screenshots/jobs/:jobId` | [docs](https://docs.allscreenshots.com/api-reference/async-jobs) |
| [List Schedules](actions/list-schedules.md) | `GET /v1/schedules` | [docs](https://docs.allscreenshots.com/api-reference/schedules) |
