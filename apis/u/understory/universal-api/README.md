# <img src="https://images.mindcloud.co/apps/icons/understory_1773950245603.png" alt="Understory logo" width="28" height="28"> Understory: Universal API

Manage Understory bookings, experiences, events, orders, and webhooks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/understory/latest
- **Category:** Commerce
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://understory.io
- **Vendor API docs:** https://developer.understory.io/apis

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/understory/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Booking

| Action | Method | Description |
| --- | --- | --- |
| [Create Booking](actions/create-booking.md) | POST | Creates a new booking in Understory. |
| [Get Booking](actions/get-booking.md) | GET | Retrieves a booking from Understory. |
| [List Bookings](actions/list-bookings.md) | GET | Retrieves bookings from Understory. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from Understory. |
| [List Events](actions/list-events.md) | GET | Retrieves events from Understory. |

### Event Availability

| Action | Method | Description |
| --- | --- | --- |
| [Get Event Availability](actions/get-event-availability.md) | GET | Retrieves event availability from Understory. |
| [List Event Availability](actions/list-event-availability.md) | GET | Retrieves event availability for an experience in Understory. |

### Experience

| Action | Method | Description |
| --- | --- | --- |
| [Get Experience](actions/get-experience.md) | GET | Retrieves an experience from Understory. |
| [List Experiences](actions/list-experiences.md) | GET | Retrieves experiences from Understory. |

### Information Request

| Action | Method | Description |
| --- | --- | --- |
| [List Information Requests](actions/list-information-requests.md) | GET | Retrieves information requests for an experience in Understory. |

### Marketing Consent

| Action | Method | Description |
| --- | --- | --- |
| [List Marketing Consents](actions/list-marketing-consents.md) | GET | Retrieves marketing consents from Understory. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from Understory. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from Understory. |

### Order Line Item

| Action | Method | Description |
| --- | --- | --- |
| [List Order Line Items](actions/list-order-line-items.md) | GET | Retrieves order line items from Understory. |

### Order Refund

| Action | Method | Description |
| --- | --- | --- |
| [List Order Refunds](actions/list-order-refunds.md) | GET | Retrieves order refunds from Understory. |

### Order Transaction

| Action | Method | Description |
| --- | --- | --- |
| [List Order Transactions](actions/list-order-transactions.md) | GET | Retrieves order transactions from Understory. |

### Ticket

| Action | Method | Description |
| --- | --- | --- |
| [List Booking Tickets](actions/list-booking-tickets.md) | GET | Retrieves tickets for a booking in Understory. |

### Ticket Variant

| Action | Method | Description |
| --- | --- | --- |
| [List Ticket Variants](actions/list-ticket-variants.md) | GET | Retrieves ticket variants for an experience in Understory. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Understory. |

### Webhook Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | POST | Creates a new webhook subscription in Understory. |
| [Delete Webhook Subscription](actions/delete-webhook-subscription.md) | DELETE | Deletes an existing webhook subscription from Understory. |
| [Get Webhook Subscription](actions/get-webhook-subscription.md) | GET | Retrieves a webhook subscription from Understory. |
| [List Webhook Subscriptions](actions/list-webhook-subscriptions.md) | GET | Retrieves webhook subscriptions from Understory. |
| [Update Webhook Subscription](actions/update-webhook-subscription.md) | PUT | Updates an existing webhook subscription in Understory. |

