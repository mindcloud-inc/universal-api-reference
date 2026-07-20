# <img src="https://images.mindcloud.co/apps/icons/ventrata_1774898407632.png" alt="Ventrata logo" width="28" height="28"> Ventrata: Universal API

Manage Ventrata OCTO suppliers, products, availability, bookings, and orders from the public reseller API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ventrata/latest
- **Category:** Commerce
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ventrata.com
- **Vendor API docs:** https://docs.ventrata.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Capabilities](actions/list-capabilities.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/list-capabilities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Availability

| Action | Method | Description |
| --- | --- | --- |
| [Get Availability](actions/get-availability.md) | GET | Retrieves availability from Ventrata. |
| [Get Availability Calendar](actions/get-availability-calendar.md) | GET | Retrieves availability calendar data from Ventrata. |
| [Get Batch Availability](actions/get-batch-availability.md) | GET | Retrieves batch availability from Ventrata. |
| [Get Batch Availability Calendar](actions/get-batch-availability-calendar.md) | GET | Retrieves batch availability calendar data from Ventrata. |

### Booking

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Booking](actions/cancel-booking.md) | DELETE | Cancels an existing booking in Ventrata. |
| [Confirm Booking](actions/confirm-booking.md) | PUT | Confirms an existing booking in Ventrata. |
| [Create and Confirm Booking](actions/create-and-confirm-booking.md) | POST | Creates and confirms a booking in Ventrata. |
| [Create Booking](actions/create-booking.md) | POST | Creates a new booking in Ventrata. |
| [Extend Reservation](actions/extend-reservation.md) | PUT | Extends an existing reservation in Ventrata. |
| [Get Booking](actions/get-booking.md) | GET | Retrieves a booking from Ventrata. |
| [List Bookings](actions/list-bookings.md) | GET | Retrieves bookings from Ventrata. |
| [Notify Booking](actions/notify-booking.md) | PUT | Sends notifications for a booking in Ventrata. |
| [Preview Booking Rebook](actions/preview-booking-rebook.md) | PUT | Previews an existing booking rebook in Ventrata. |
| [Preview Booking Update](actions/preview-booking-update.md) | PUT | Previews an existing booking update in Ventrata. |
| [Rebook Booking](actions/rebook-booking.md) | PUT | Rebooks an existing booking in Ventrata. |
| [Update Booking](actions/update-booking.md) | PUT | Updates an existing booking in Ventrata. |

### Capability

| Action | Method | Description |
| --- | --- | --- |
| [List Capabilities](actions/list-capabilities.md) | GET | Retrieves capabilities from Ventrata. |

### Connection

| Action | Method | Description |
| --- | --- | --- |
| [Who Am I](actions/who-am-i.md) | GET | Retrieves reseller connection details from Ventrata. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Confirm Order](actions/confirm-order.md) | PUT | Confirms an existing order in Ventrata. |
| [Create Order](actions/create-order.md) | POST | Creates a new order in Ventrata. |
| [Delete Order](actions/delete-order.md) | DELETE | Deletes an existing order from Ventrata. |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from Ventrata. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from Ventrata. |
| [Notify Order](actions/notify-order.md) | PUT | Sends notifications for an order in Ventrata. |
| [Preview Order Update](actions/preview-order-update.md) | PUT | Previews an existing order update in Ventrata. |
| [Update Order](actions/update-order.md) | PUT | Updates an existing order in Ventrata. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from Ventrata. |
| [List Products](actions/list-products.md) | GET | Retrieves products from Ventrata. |

### Supplier

| Action | Method | Description |
| --- | --- | --- |
| [Get Supplier](actions/get-supplier.md) | GET | Retrieves a supplier from Ventrata. |
| [List Suppliers](actions/list-suppliers.md) | GET | Retrieves suppliers from Ventrata. |

