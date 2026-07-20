# Fraser Direct: Native API Reference

A consolidated summary of Fraser Direct's API configuration and 7 documented operations.

- **API base URL:** `https://apiv2test.fraserdirect.ca/`

## Authentication

### Custom

Bearer token authentication using Fraser Direct's password-grant token endpoint.

### Credentials

- **Username:** `username` · required · Fraser Direct API login username.
- **Password:** `password` · required · Fraser Direct API password.

Send these headers with each API request:

```http
Authorization: Bearer <custom.accessToken>
```

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Endpoints (7 documented)

| Operation | Method & path |
| --- | --- |
| [Create order](actions/create-order.md) | `POST /CreateOrder` |
| [Create purchase order](actions/create-purchase-order.md) | `POST /CreatePO` |
| [Get inventory](actions/get-inventory.md) | `GET /GetInventory` |
| [Get inventory adjustments](actions/get-inventory-adjustments.md) | `GET /GetInventoryAdjustments` |
| [Get order information](actions/get-order-information.md) | `GET /GetOrderInformation` |
| [Get order shipping information](actions/get-order-shipping-information.md) | `GET /GetOrderShippingInformation` |
| [Get purchase order information](actions/get-purchase-order-information.md) | `GET /GetPOInformation` |
