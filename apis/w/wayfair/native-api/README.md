# Wayfair: Native API Reference

A consolidated summary of Wayfair's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://developer.wayfair.io/posts/introduction
- **API base URL:** `https://{environment}.com/v1/`

## Authentication

### Custom

### Credentials

- **Client Secret:** `clientSecret` · optional
- **Client Id:** `clientId` · optional
- **Environment:** `environment` · optional

Send these headers with each API request:

```http
Authorization: Bearer <custom.accessToken>
```

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Accept Order](actions/accept-order.md) | `POST graphql` |  |
| [Acknowledge Castle Gate Order](actions/acknowledge-castle-gate-order.md) | `POST graphql` |  |
| [Acknowledge CastleGate Shipping Advice](actions/acknowledge-castle-gate-shipping-advice.md) | `POST graphql` |  |
| [Get Bill of Lading](actions/get-bill-of-lading.md) | `GET bill_of_lading/:purchaseOrderNumber` |  |
| [Get CastleGate Orders](actions/get-castle-gate-orders.md) | `POST graphql` | [docs](https://developer.wayfair.com/docs/#castlegate-order-query) |
| [Get CastleGate Orders Shipping Advice](actions/get-castle-gate-shipping-advice.md) | `POST graphql` |  |
| [Get Dropship Orders](actions/get-dropship-orders.md) | `POST graphql` |  |
| [Get Packing Slip](actions/get-packing-slip.md) | `GET packing_slip/:purchaseOrderNumber` |  |
| [Get Shipping Label](actions/get-shipping-label.md) | `GET shipping_label/:purchaseOrderNumber` |  |
| [GraphQL](actions/graph-ql.md) | `POST graphql` |  |
| [Register Order](actions/register-order.md) | `POST graphql` |  |
| [Send Shipment Notice](actions/send-shipment-notice.md) | `POST graphql` |  |
| [test](actions/test.md) | `GET https://sandbox.api.wayfair.com/v1/demo/clock` |  |
| [Update Item List Inventory](actions/update-inventory-list.md) | `POST graphql` |  |
