# Layer4: Native API Reference

A consolidated summary of Layer4's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://www.layer4.app/api-docs
- **OpenAPI specification:** https://www.layer4.app/api-docs/swagger.json
- **API base URL:** `https://www.layer4.app`

## Authentication

### Workspace API Key

Authenticate Layer4 API requests with a workspace API key from the Layer4 dashboard.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.layer4.app/api-keys/create-api-key/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `data.meta.totalPagesCount`. The current page number is read from `data.meta.page`.

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Async Create Record](actions/async-create-record.md) | `POST /api/v1/buckets/:bucketId/async/records` |  |
| [Create Record](actions/create-record.md) | `POST /api/v1/buckets/:bucketId/records` |  |
| [Create Token](actions/create-token.md) | `POST /api/v1/buckets/:bucketId/tokens` |  |
| [Get Record](actions/get-record.md) | `GET /api/v1/buckets/:bucketId/records/:recordId` |  |
| [Get Record Request](actions/get-record-request.md) | `GET /api/v1/buckets/:bucketId/record-requests/:recordRequestId` |  |
| [Get Token](actions/get-token.md) | `GET /api/v1/buckets/:bucketId/tokens/:tokenId` | [docs](https://www.layer4.app/api-docs#tag/Tokens/operation/TokensController_findOne) |
| [Get Token Metadata](actions/get-token-metadata.md) | `GET /api/v1/buckets/:bucketId/tokens/:tokenId/metadata` | [docs](https://www.layer4.app/api-docs#tag/Tokens/operation/TokensController_findMetadata) |
| [Get Token Request](actions/get-token-request.md) | `GET /api/v1/buckets/:bucketId/token-requests/:tokenRequestId` | [docs](https://www.layer4.app/api-docs#tag/Token-Requests/operation/TokenRequestsController_findOne) |
| [Get Token Supply](actions/get-token-supply.md) | `GET /api/v1/buckets/:bucketId/tokens/:tokenId/supply` | [docs](https://www.layer4.app/api-docs#tag/Tokens/operation/TokensController_findSupply) |
| [List Record Requests](actions/list-record-requests.md) | `GET /api/v1/buckets/:bucketId/record-requests` | [docs](https://www.layer4.app/api-docs#tag/Record-Requests/operation/RecordRequestsController_findAll) |
| [List Records](actions/list-records.md) | `GET /api/v1/buckets/:bucketId/records` | [docs](https://www.layer4.app/api-docs#tag/Records/operation/RecordsController_findAll) |
| [List Token Requests](actions/list-token-requests.md) | `GET /api/v1/buckets/:bucketId/token-requests` | [docs](https://www.layer4.app/api-docs#tag/Token-Requests/operation/TokenRequestsController_findAll) |
| [List Tokens](actions/list-tokens.md) | `GET /api/v1/buckets/:bucketId/tokens` | [docs](https://www.layer4.app/api-docs#tag/Tokens/operation/TokensController_findAll) |
| [List Wallets](actions/list-wallets.md) | `GET /api/v1/wallets` | [docs](https://www.layer4.app/api-docs#tag/Wallets/operation/WalletsController_findAll) |
