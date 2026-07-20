# Ventrata: Native API Reference

A consolidated summary of Ventrata's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.ventrata.com/
- **API base URL:** `https://api.ventrata.com`

## Authentication

### API Key

Use the Ventrata OCTO reseller API key for a single supplier connection.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.ventrata.com/getting-started/getting-started)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Booking](actions/cancel-booking.md) | `POST octo/bookings/:uuid/cancel` | [docs](https://docs.ventrata.com/octo-core/bookings#post-bookings-uuid-cancel) |
| [Confirm Booking](actions/confirm-booking.md) | `POST octo/bookings/:uuid/confirm` | [docs](https://docs.ventrata.com/octo-core/bookings#post-bookings-uuid-confirm) |
| [Confirm Order](actions/confirm-order.md) | `POST octo/orders/:orderId/confirm` | [docs](https://docs.ventrata.com/capabilities/cart#post-orders-orderid-confirm) |
| [Create and Confirm Booking](actions/create-and-confirm-booking.md) | `POST octo/bookings/confirm` | [docs](https://docs.ventrata.com/octo-core/bookings) |
| [Create Booking](actions/create-booking.md) | `POST octo/bookings` | [docs](https://docs.ventrata.com/octo-core/bookings#post-bookings) |
| [Create Order](actions/create-order.md) | `POST octo/orders` | [docs](https://docs.ventrata.com/capabilities/cart#post-orders) |
| [Delete Order](actions/delete-order.md) | `DELETE octo/orders/:orderId` | [docs](https://docs.ventrata.com/capabilities/cart#delete-orders-orderid) |
| [Extend Reservation](actions/extend-reservation.md) | `POST octo/bookings/:uuid/extend` | [docs](https://docs.ventrata.com/octo-core/bookings#post-bookings-uuid-extend) |
| [Get Availability](actions/get-availability.md) | `POST octo/availability` | [docs](https://docs.ventrata.com/octo-core/availability#post-availability) |
| [Get Availability Calendar](actions/get-availability-calendar.md) | `POST octo/availability/calendar` | [docs](https://docs.ventrata.com/octo-core/availability#post-availability-calendar) |
| [Get Batch Availability](actions/get-batch-availability.md) | `POST octo/availability/batch` | [docs](https://docs.ventrata.com/octo-core/availability#post-availability-batch) |
| [Get Batch Availability Calendar](actions/get-batch-availability-calendar.md) | `POST octo/availability/calendar/batch` | [docs](https://docs.ventrata.com/octo-core/availability#post-availability-calendar-batch) |
| [Get Booking](actions/get-booking.md) | `GET octo/bookings/:uuid` | [docs](https://docs.ventrata.com/octo-core/bookings#get-bookings-uuid) |
| [Get Order](actions/get-order.md) | `GET octo/orders/:orderId` | [docs](https://docs.ventrata.com/capabilities/cart#get-orders-orderid) |
| [Get Product](actions/get-product.md) | `GET octo/products/:productId` | [docs](https://docs.ventrata.com/octo-core/products#get-products-productid) |
| [Get Supplier](actions/get-supplier.md) | `GET octo/suppliers/:supplierId` | [docs](https://docs.ventrata.com/octo-core/suppliers) |
| [List Bookings](actions/list-bookings.md) | `GET octo/bookings` | [docs](https://docs.ventrata.com/octo-core/bookings#get-bookings) |
| [List Capabilities](actions/list-capabilities.md) | `GET octo/capabilities` | [docs](https://docs.ventrata.com/getting-started/request-capabilities#get-capabilities) |
| [List Orders](actions/list-orders.md) | `GET octo/orders` | [docs](https://docs.ventrata.com/capabilities/cart#get-orders) |
| [List Products](actions/list-products.md) | `GET octo/products` | [docs](https://docs.ventrata.com/octo-core/products#get-products) |
| [List Suppliers](actions/list-suppliers.md) | `GET octo/suppliers` | [docs](https://docs.ventrata.com/octo-core/suppliers) |
| [Notify Booking](actions/notify-booking.md) | `POST octo/bookings/:uuid/notify` | [docs](https://docs.ventrata.com/octo-core/bookings) |
| [Notify Order](actions/notify-order.md) | `POST octo/orders/:orderId/notify` | [docs](https://docs.ventrata.com/capabilities/cart#post-orders-orderid-notify) |
| [Preview Booking Rebook](actions/preview-booking-rebook.md) | `POST octo/bookings/:uuid/rebook/preview` | [docs](https://docs.ventrata.com/octo-core/bookings) |
| [Preview Booking Update](actions/preview-booking-update.md) | `PATCH octo/bookings/:uuid/preview` | [docs](https://docs.ventrata.com/octo-core/bookings) |
| [Preview Order Update](actions/preview-order-update.md) | `PATCH octo/orders/:orderId/preview` | [docs](https://docs.ventrata.com/capabilities/cart#patch-orders-orderid-preview) |
| [Rebook Booking](actions/rebook-booking.md) | `POST octo/bookings/:uuid/rebook` | [docs](https://docs.ventrata.com/octo-core/bookings) |
| [Update Booking](actions/update-booking.md) | `PATCH octo/bookings/:uuid` | [docs](https://docs.ventrata.com/octo-core/bookings#patch-bookings-uuid) |
| [Update Order](actions/update-order.md) | `PATCH octo/orders/:orderId` | [docs](https://docs.ventrata.com/capabilities/cart#patch-orders-orderid) |
| [Who Am I](actions/who-am-i.md) | `GET octo/whoami` | [docs](https://docs.ventrata.com/getting-started/request-capabilities#get-whoami) |
