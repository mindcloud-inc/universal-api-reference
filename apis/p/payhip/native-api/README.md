# Payhip: Native API Reference

A consolidated summary of Payhip's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://payhip.com/api-reference
- **API base URL:** `https://payhip.com/api/v2`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required
- **Product Secret Key:** `productSecretKey` · optional · Required only for Payhip license key endpoints.

Send these headers with each API request:

```http
payhip-api-key: <apiKey>
product-secret-key: <productSecretKey>
```

[Official authentication documentation](https://payhip.com/api-reference)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Coupon](actions/create-coupon.md) | `POST /coupons` | [docs](https://payhip.com/api-reference/coupons/create) |
| [Decrease License Usage](actions/decrease-license-usage.md) | `PUT /license/decrease` | [docs](https://payhip.com/api-reference/license-keys/usage-decrease) |
| [Disable License Key](actions/disable-license-key.md) | `PUT /license/disable` | [docs](https://payhip.com/api-reference/license-keys/disable) |
| [Enable License Key](actions/enable-license-key.md) | `PUT /license/enable` | [docs](https://payhip.com/api-reference/license-keys/enable) |
| [Get Coupon](actions/get-coupon.md) | `GET /coupons/:coupon_id` | [docs](https://payhip.com/api-reference/coupons/retrieve) |
| [Increase License Usage](actions/increase-license-usage.md) | `PUT /license/usage` | [docs](https://payhip.com/api-reference/license-keys/usage-increase) |
| [List Coupons](actions/list-coupons.md) | `GET /coupons` | [docs](https://payhip.com/api-reference/coupons/list) |
| [Verify License Key](actions/verify-license-key.md) | `GET /license/verify` | [docs](https://payhip.com/api-reference/license-keys/retrieve) |
