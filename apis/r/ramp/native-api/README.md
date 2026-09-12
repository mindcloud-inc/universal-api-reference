# Ramp: Native API Reference

A consolidated summary of Ramp's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://docs.ramp.com/developer-api/v1/overview/introduction
- **API base URL:** `https://api.ramp.com/developer/v1/`

## Authentication

### Custom

Token Based

### Credentials

- **Client ID:** `clientID` · required
- **Client Secret:** `clientSecret` · required

Send these headers with each API request:

```http
Authorization: Bearer <custom.accessToken>
```

[Official authentication documentation](https://docs.ramp.com/developer-api/v1/api/authorization)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

The next-page cursor is read from `page.next`.

## Pagination

Use `page_size` in the query string to set the page size (default 100; accepted range 2–100). Follow the complete next-page URL returned by the API.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Transaction](actions/get-transaction.md) | `GET transactions/:transactionId` | [docs](https://docs.ramp.com/developer-api/v1/api/transactions#get-developer-v1-transactions-transaction-id) |
| [List Purchase Orders](actions/list-purchase-orders.md) | `GET transactions` | [docs](https://docs.ramp.com/developer-api/v1/api/transactions) |
| [List Receipts](actions/list-receipts.md) | `GET receipts` | [docs](https://docs.ramp.com/developer-api/v1/api/receipts) |
| [List Transactions](actions/list-transactions.md) | `GET transactions` | [docs](https://docs.ramp.com/developer-api/v1/api/transactions) |
| [List Vendors](actions/list-vendors.md) | `GET vendors` | [docs](https://docs.ramp.com/developer-api/v1/api/vendors) |
| [Verify Webhook Endpoint](actions/new-action1.md) | `POST webhooks/:webhookId/verify` | [docs](https://docs.ramp.com/developer-api/v1/webhooks) |
| [Subscribe To Events](actions/subscribe-to-events.md) | `POST webhooks` |  |
| [Upload a new memo for a transaction](actions/upload-transaction-memo.md) | `POST memos/:transactionId` | [docs](https://docs.ramp.com/developer-api/v1/api/transactions#get-developer-v1-transactions-transaction-id) |
