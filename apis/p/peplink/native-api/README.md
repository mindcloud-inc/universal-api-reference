# Peplink: Native API Reference

A consolidated summary of Peplink's API configuration and 7 documented operations.

- **API base URL:** `https://portal.peplink.com/api/e/v1/cp/`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Devices](actions/check-devices.md) | `GET devices/check` | [docs](https://portal.peplink.com/docs/api-reference/devices/search/) |
| [Create Order](actions/create-order.md) | `POST orders` |  |
| [Create Order PO File](actions/create-order-po-file.md) | `POST orders/:orderNumber/customer-po-files` | [docs](https://portal.peplink.com/docs/api-reference/orders/customer-po-files/create/) |
| [Get Order](actions/get-order.md) | `GET orders/:orderNumber` |  |
| [List All Products](actions/list-all-products.md) | `GET partner/partner-store-products` |  |
| [Search Devices](actions/search-devices.md) | `GET devices/search` | [docs](https://portal.peplink.com/docs/api-reference/devices/search/) |
| [Update customer PO number](actions/update-customer-po-number.md) | `POST /orders/:orderNumber/customer-po-number` |  |
