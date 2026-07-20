# ClearBounce: Native API Reference

A consolidated summary of ClearBounce's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://docs.clearbounce.net/api-reference/authentication
- **API base URL:** `https://api.clearbounce.net/api/v1`

## Authentication

### ClearBounce API Key

Authenticate using a ClearBounce API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://docs.clearbounce.net/api-reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Batch Verification Job](actions/create-batch-verification-job.md) | `POST /bulk/upload` | [docs](https://docs.clearbounce.net/api-reference/batch-verification) |
| [Get Batch Verification Job](actions/get-batch-verification-job.md) | `GET /bulk/status/:jobId` | [docs](https://docs.clearbounce.net/api-reference/batch-verification) |
| [Get Batch Verification Results](actions/get-batch-verification-results.md) | `GET /bulk/results/:jobId` | [docs](https://docs.clearbounce.net/api-reference/batch-verification) |
| [Get Batch Verification Results Raw](actions/get-batch-verification-results-raw.md) | `GET /bulk/results/:jobId` | [docs](https://docs.clearbounce.net/api-reference/batch-verification) |
| [Verify Email](actions/verify-email.md) | `POST /verify` | [docs](https://docs.clearbounce.net/api-reference/single-verification) |
