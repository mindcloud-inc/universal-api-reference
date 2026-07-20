# EasyPost: Native API Reference

A consolidated summary of EasyPost's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.easypost.com/
- **API base URL:** `https://api.easypost.com/v2`

## Authentication

### API Key

Use an EasyPost API key. EasyPost authenticates requests with the API key as the Basic Auth username and an empty password.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.easypost.com/docs/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page_size` in the query string to set the page size (default 20; accepted range 1–100). Use `before_id` in the query string as the pagination cursor.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Shipments To Batch](actions/add-shipments-to-batch.md) | `POST /batches/:id/add_shipments` | [docs](https://docs.easypost.com/docs/batches) |
| [Buy Batch](actions/buy-batch.md) | `POST /batches/:id/buy` | [docs](https://docs.easypost.com/docs/batches) |
| [Buy Order](actions/buy-order.md) | `POST /orders/:id/buy` | [docs](https://docs.easypost.com/docs/orders) |
| [Buy Pickup](actions/buy-pickup.md) | `POST /pickups/:id/buy` | [docs](https://docs.easypost.com/docs/pickups) |
| [Buy Shipment](actions/buy-shipment.md) | `POST /shipments/:id/buy` | [docs](https://docs.easypost.com/docs/shipments) |
| [Cancel Pickup](actions/cancel-pickup.md) | `POST /pickups/:id/cancel` | [docs](https://docs.easypost.com/docs/pickups) |
| [Create Address](actions/create-address.md) | `POST /addresses` | [docs](https://docs.easypost.com/docs/addresses) |
| [Create And Verify Address](actions/create-and-verify-address.md) | `POST /addresses/create_and_verify` | [docs](https://docs.easypost.com/docs/addresses) |
| [Create Batch](actions/create-batch.md) | `POST /batches` | [docs](https://docs.easypost.com/docs/batches) |
| [Create Batch Label](actions/create-batch-label.md) | `POST /batches/:id/label` | [docs](https://docs.easypost.com/docs/batches) |
| [Create Batch Scan Form](actions/create-batch-scan-form.md) | `POST /batches/:id/scan_form` | [docs](https://docs.easypost.com/docs/batches) |
| [Create Customs Info](actions/create-customs-info.md) | `POST /customs_infos` | [docs](https://docs.easypost.com/docs/customs-infos) |
| [Create Customs Item](actions/create-customs-item.md) | `POST /customs_items` | [docs](https://docs.easypost.com/docs/customs-items) |
| [Create Order](actions/create-order.md) | `POST /orders` | [docs](https://docs.easypost.com/docs/orders) |
| [Create Parcel](actions/create-parcel.md) | `POST /parcels` | [docs](https://docs.easypost.com/docs/parcels) |
| [Create Pickup](actions/create-pickup.md) | `POST /pickups` | [docs](https://docs.easypost.com/docs/pickups) |
| [Create Refund](actions/create-refund.md) | `POST /refunds` | [docs](https://docs.easypost.com/docs/refunds) |
| [Create Shipment](actions/create-shipment.md) | `POST /shipments` | [docs](https://docs.easypost.com/docs/shipments) |
| [Create Shipment Form](actions/create-shipment-form.md) | `POST /shipments/:id/forms` | [docs](https://docs.easypost.com/docs/shipments/forms) |
| [Create Tracker](actions/create-tracker.md) | `POST /trackers` | [docs](https://docs.easypost.com/docs/trackers) |
| [Get Address](actions/get-address.md) | `GET /addresses/:id` | [docs](https://docs.easypost.com/docs/addresses) |
| [Get Batch](actions/get-batch.md) | `GET /batches/:id` | [docs](https://docs.easypost.com/docs/batches) |
| [Get Customs Info](actions/get-customs-info.md) | `GET /customs_infos/:id` | [docs](https://docs.easypost.com/docs/customs-infos) |
| [Get Customs Item](actions/get-customs-item.md) | `GET /customs_items/:id` | [docs](https://docs.easypost.com/docs/customs-items) |
| [Get Order](actions/get-order.md) | `GET /orders/:id` | [docs](https://docs.easypost.com/docs/orders) |
| [Get Parcel](actions/get-parcel.md) | `GET /parcels/:id` | [docs](https://docs.easypost.com/docs/parcels) |
| [Get Pickup](actions/get-pickup.md) | `GET /pickups/:id` | [docs](https://docs.easypost.com/docs/pickups) |
| [Get Refund](actions/get-refund.md) | `GET /refunds/:id` | [docs](https://docs.easypost.com/docs/refunds) |
| [Get Shipment](actions/get-shipment.md) | `GET /shipments/:id` | [docs](https://docs.easypost.com/docs/shipments) |
| [Get Shipment Label](actions/get-shipment-label.md) | `GET /shipments/:id/label` | [docs](https://docs.easypost.com/docs/shipments) |
| [Get Tracker](actions/get-tracker.md) | `GET /trackers/:id` | [docs](https://docs.easypost.com/docs/trackers) |
| [Insure Shipment](actions/insure-shipment.md) | `POST /shipments/:id/insure` | [docs](https://docs.easypost.com/docs/shipments/shipping-insurance) |
| [List Addresses](actions/list-addresses.md) | `GET /addresses` | [docs](https://docs.easypost.com/docs/addresses) |
| [List Batches](actions/list-batches.md) | `GET /batches` | [docs](https://docs.easypost.com/docs/batches) |
| [List Pickups](actions/list-pickups.md) | `GET /pickups` | [docs](https://docs.easypost.com/docs/pickups) |
| [List Refunds](actions/list-refunds.md) | `GET /refunds` | [docs](https://docs.easypost.com/docs/refunds) |
| [List Shipments](actions/list-shipments.md) | `GET /shipments` | [docs](https://docs.easypost.com/docs/shipments) |
| [List Trackers](actions/list-trackers.md) | `GET /trackers` | [docs](https://docs.easypost.com/docs/trackers) |
| [Remove Shipments From Batch](actions/remove-shipments-from-batch.md) | `POST /batches/:id/remove_shipments` | [docs](https://docs.easypost.com/docs/batches) |
| [Rerate Shipment](actions/rerate-shipment.md) | `POST /shipments/:id/rerate` | [docs](https://docs.easypost.com/docs/shipments/rates) |
