# Geral: Native API Reference

A consolidated summary of Geral's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://ger.al/api-documentation
- **API base URL:** `https://ger.al/api`

## Authentication

### Bearer API Key

Use the API key from the Geral account API page as a Bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://ger.al/api-documentation)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `results_per_page` in the query string to set the page size (default 25; accepted range 10–1000). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `contains`, `eq`.

## Sorting

Set the sort field with `order_by` in the query string. Set the direction separately with `order_type`. Use `ASC` for ascending order and `DESC` for descending order. Only one sort field is accepted.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Domain](actions/delete-domain.md) | `DELETE /domains/:domain_id` | [docs](https://ger.al/api-documentation/domains) |
| [Delete Link](actions/delete-link.md) | `DELETE /links/:link_id` | [docs](https://ger.al/api-documentation/links) |
| [Delete Pixel](actions/delete-pixel.md) | `DELETE /pixels/:pixel_id` | [docs](https://ger.al/api-documentation/pixels) |
| [Delete QR Code](actions/delete-qr-code.md) | `DELETE /qr-codes/:qr_code_id` | [docs](https://ger.al/api-documentation/qr-codes) |
| [Get Collected Data](actions/get-collected-data.md) | `GET /data/:datum_id` | [docs](https://ger.al/api-documentation/data) |
| [Get Domain](actions/get-domain.md) | `GET /domains/:domain_id` | [docs](https://ger.al/api-documentation/domains) |
| [Get Link](actions/get-link.md) | `GET /links/:link_id` | [docs](https://ger.al/api-documentation/links) |
| [Get Link Statistics](actions/get-link-statistics.md) | `GET /statistics/:link_id` | [docs](https://ger.al/api-documentation/statistics) |
| [Get Notification Handler](actions/get-notification-handler.md) | `GET /notification-handlers/:notification_handler_id` | [docs](https://ger.al/api-documentation/notification-handlers) |
| [Get Payment](actions/get-payment.md) | `GET /payments/:payment_id` | [docs](https://ger.al/api-documentation/payments) |
| [Get Pixel](actions/get-pixel.md) | `GET /pixels/:pixel_id` | [docs](https://ger.al/api-documentation/pixels) |
| [Get QR Code](actions/get-qr-code.md) | `GET /qr-codes/:qr_code_id` | [docs](https://ger.al/api-documentation/qr-codes) |
| [Get Splash Page](actions/get-splash-page.md) | `GET /splash-pages/:splash_page_id` | [docs](https://ger.al/api-documentation/splash-pages) |
| [Get User](actions/get-user.md) | `GET /user` | [docs](https://ger.al/api-documentation/user) |
| [List Account Logs](actions/list-account-logs.md) | `GET /logs/` | [docs](https://ger.al/api-documentation/users-logs) |
| [List Collected Data](actions/list-collected-data.md) | `GET /data/` | [docs](https://ger.al/api-documentation/data) |
| [List Domains](actions/list-domains.md) | `GET /domains/` | [docs](https://ger.al/api-documentation/domains) |
| [List Links](actions/list-links.md) | `GET /links/` | [docs](https://ger.al/api-documentation/links) |
| [List Notification Handlers](actions/list-notification-handlers.md) | `GET /notification-handlers/` | [docs](https://ger.al/api-documentation/notification-handlers) |
| [List Payments](actions/list-payments.md) | `GET /payments/` | [docs](https://ger.al/api-documentation/payments) |
| [List Pixels](actions/list-pixels.md) | `GET /pixels/` | [docs](https://ger.al/api-documentation/pixels) |
| [List QR Codes](actions/list-qr-codes.md) | `GET /qr-codes/` | [docs](https://ger.al/api-documentation/qr-codes) |
| [List Splash Pages](actions/list-splash-pages.md) | `GET /splash-pages/` | [docs](https://ger.al/api-documentation/splash-pages) |
| [List Statistics](actions/list-statistics.md) | `GET /statistics/` | [docs](https://ger.al/api-documentation/statistics) |
