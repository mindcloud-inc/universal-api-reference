# Proofy: Native API Reference

A consolidated summary of Proofy's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://docs.proofy.io/
- **API base URL:** `https://apis.proofy.io/v1`

## Authentication

### API Key

Connect with a Proofy API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.proofy.io/usage)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Batch Status](actions/check-batch-status.md) | `GET /verify/batch/:id` | [docs](https://docs.proofy.io/api-reference/endpoint/verify-batch-status) |
| [Check File Status](actions/check-file-status.md) | `GET /verify/file/:id` | [docs](https://docs.proofy.io/api-reference/endpoint/verify-file-status) |
| [Create Batch Request](actions/create-batch-request.md) | `POST /verify/batch/create` | [docs](https://docs.proofy.io/api-reference/endpoint/verify-batch-create) |
| [Delete Batch Request](actions/delete-batch-request.md) | `DELETE /verify/batch/:id` | [docs](https://docs.proofy.io/api-reference/endpoint/verify-batch-cancel) |
| [Delete File](actions/delete-file.md) | `DELETE /verify/file/:id` | [docs](https://docs.proofy.io/api-reference/endpoint/verify-file-cancel) |
| [Download File Results](actions/download-file-results.md) | `GET /verify/file/:id/download` | [docs](https://docs.proofy.io/api-reference/endpoint/verify-file-download) |
| [Get Available Credits](actions/get-available-credits.md) | `GET /credits` | [docs](https://docs.proofy.io/api-reference/endpoint/credits) |
| [Get Batch Results](actions/get-batch-results.md) | `GET /verify/batch/:id/download` | [docs](https://docs.proofy.io/api-reference/endpoint/verify-batch-download) |
| [Upload File](actions/upload-file.md) | `POST /verify/file/upload` | [docs](https://docs.proofy.io/api-reference/endpoint/verify-file-upload) |
| [Upload File by URL](actions/upload-file-by-url.md) | `POST /verify/file/create` | [docs](https://docs.proofy.io/api-reference/endpoint/verify-file-create) |
| [Verify Single Email](actions/verify-single-email.md) | `GET /verify/single` | [docs](https://docs.proofy.io/api-reference/endpoint/verify-single) |
