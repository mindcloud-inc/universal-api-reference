# CallerAPI: Native API Reference

A consolidated summary of CallerAPI's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://docs.callerapi.com/
- **API base URL:** `https://api.callerapi.com`

## Authentication

### API Key

Authenticate with a CallerAPI API key passed in the x-auth header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.callerapi.com/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `page_size` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Balance and Email](actions/get-balance-and-email.md) | `GET /api/me` | [docs](https://docs.callerapi.com/balance-and-email-20033243e0) |
| [List Webhook Subscriptions](actions/list-webhook-subscriptions.md) | `GET /api/webhooks/complaints/subscriptions` | [docs](https://docs.callerapi.com/list-webhook-subscriptions-22518650e0) |
| [Lookup Spam Score and HLR](actions/lookup-spam-score-and-hlr.md) | `GET /api/lookup/:phone` | [docs](https://docs.callerapi.com/spam-score-hlr-19887237e0) |
