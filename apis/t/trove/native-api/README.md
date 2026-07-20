# Trove: Native API Reference

A consolidated summary of Trove's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://trove.headline.com/docs
- **API base URL:** `https://trove.headline.com/api/v1`

## Authentication

### API Key

Authenticate requests with your Trove API key in the X-API-KEY header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://trove.headline.com/docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Enrich Bulk Transactions](actions/enrich-bulk-transactions.md) | `POST /transactions/bulk` | [docs](https://trove.headline.com/docs) |
| [Enrich Sample Transaction](actions/enrich-sample-transaction.md) | `POST /transactions/enrich` | [docs](https://trove.headline.com/docs) |
| [Get Bulk Transaction Result](actions/get-bulk-transaction-result.md) | `GET /transactions/bulk/:requestId` | [docs](https://trove.headline.com/docs) |
| [Submit Enrichment Feedback](actions/submit-enrichment-feedback.md) | `POST /transactions/feedback` | [docs](https://trove.headline.com/docs) |
