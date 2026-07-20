# Soundee: Native API Reference

A consolidated summary of Soundee's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://soundee.readme.io/reference/introduction
- **API base URL:** `https://api.soundee.com/me`

## Authentication

### API Key

Connect to the Soundee Producer API with a Soundee API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://soundee.readme.io/reference/authentication)

## API conventions

Responses from this API use JSON. Response data is read from `response.data`.

## Pagination

Use `limit` in the query string to set the page size (default 30; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Coupon](actions/create-coupon.md) | `POST /coupons` | [docs](https://soundee.readme.io/reference/create) |
| [Get Account](actions/get-account.md) | `GET /` | [docs](https://soundee.readme.io/reference/me-1) |
| [Get Cart Abandonment](actions/get-cart-abandonment.md) | `GET /cart-abandonments/:idOrToken` | [docs](https://soundee.readme.io/reference/get-abandoned-cart-object) |
| [Get Coupon](actions/get-coupon.md) | `GET /coupons/:id` | [docs](https://soundee.readme.io/reference/get-transaction-object) |
| [Get Transaction](actions/get-transaction.md) | `GET /transactions/:id` | [docs](https://soundee.readme.io/reference/get-by-id-1) |
| [List Cart Abandonments](actions/list-cart-abandonments.md) | `GET /cart-abandonments` | [docs](https://soundee.readme.io/reference/read-list-1) |
| [List Coupons](actions/list-coupons.md) | `GET /coupons` | [docs](https://soundee.readme.io/reference/get) |
| [List Email Captures](actions/list-email-captures.md) | `GET /email-captures` | [docs](https://soundee.readme.io/reference/read-2) |
| [List Transactions](actions/list-transactions.md) | `GET /transactions` | [docs](https://soundee.readme.io/reference/get-2) |
| [Update Coupon](actions/update-coupon.md) | `PUT /coupons/:id` | [docs](https://soundee.readme.io/reference/update) |
