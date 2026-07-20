# Shipday: Native API Reference

A consolidated summary of Shipday's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://docs.shipday.com/reference/shipday-api
- **API base URL:** `https://api.shipday.com`

## Authentication

### API Key

Connect using your Shipday API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.shipday.com/reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Carrier](actions/add-carrier.md) | `POST /carriers` | [docs](https://docs.shipday.com/reference/add-a-carrier-1) |
| [Assign Order to Driver](actions/assign-order-to-driver.md) | `PUT /orders/assign/:orderId/:carrierId` | [docs](https://docs.shipday.com/reference/assign-order) |
| [Availability](actions/availability.md) | `POST /on-demand/availability` | [docs](https://docs.shipday.com/reference/availability-1) |
| [Create Order](actions/create-order.md) | `POST /orders` | [docs](https://docs.shipday.com/reference/insert-delivery-order) |
| [Delete Order](actions/delete-order.md) | `DELETE /orders/:orderId` | [docs](https://docs.shipday.com/reference/delete-order) |
| [Get Estimate](actions/get-estimate.md) | `GET /on-demand/estimate/:orderId` | [docs](https://docs.shipday.com/reference/estimate) |
| [List Active Orders](actions/list-active-orders.md) | `GET /orders` | [docs](https://docs.shipday.com/reference/retrieve-active-orders) |
| [List Carriers](actions/list-carriers.md) | `GET /carriers` | [docs](https://docs.shipday.com/reference/retrieve-carriers) |
| [List Services](actions/list-services.md) | `GET /on-demand/services` | [docs](https://docs.shipday.com/reference/services) |
| [Retrieve Order Delivery Progress](actions/retrieve-order-delivery-progress.md) | `GET /order/progress/:trackingId` | [docs](https://docs.shipday.com/reference/order-delivery-progress) |
| [Retrieve Order Details](actions/retrieve-order-details.md) | `GET /orders/:orderNumber` | [docs](https://docs.shipday.com/reference/retrieve-order-details) |
| [Search Delivery Orders](actions/search-delivery-orders.md) | `POST /orders/query` | [docs](https://docs.shipday.com/reference/delivery-orders-query) |
| [Set Order Ready to Pickup](actions/set-order-ready-to-pickup.md) | `PUT /orders/:orderId/meta` | [docs](https://docs.shipday.com/reference/order-ready-to-pickup) |
| [Unassign Order from Driver](actions/unassign-order-from-driver.md) | `PUT /orders/unassign/:orderId` | [docs](https://docs.shipday.com/reference/unassign-order-from-driver-1) |
| [Update Order Status](actions/update-order-status.md) | `PUT /orders/:orderId/status` | [docs](https://docs.shipday.com/reference/order-status-update) |
