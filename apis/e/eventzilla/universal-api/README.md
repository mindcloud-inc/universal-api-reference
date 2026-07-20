# <img src="https://images.mindcloud.co/apps/icons/eventzilla_1774376576981.png" alt="Eventzilla logo" width="28" height="28"> Eventzilla: Universal API

Manage events, attendees, orders, and check-ins

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/eventzilla/latest
- **Category:** Marketing / Events & Webinars
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.eventzilla.net
- **Vendor API docs:** https://developer.eventzilla.net/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Events](actions/list-events.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Attendee

| Action | Method | Description |
| --- | --- | --- |
| [Get Attendee](actions/get-attendee.md) | GET | Retrieves an attendee from Eventzilla. |
| [List Event Attendees](actions/list-event-attendees.md) | GET | Retrieves attendees for an event from Eventzilla. |
| [Update Attendee Check-In](actions/update-attendee-check-in.md) | PUT | Updates attendee check-in status in Eventzilla. |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [List Categories](actions/list-categories.md) | GET | Retrieves categories from Eventzilla. |

### Checkout

| Action | Method | Description |
| --- | --- | --- |
| [Confirm Checkout](actions/confirm-checkout.md) | PUT | Confirms a checkout in Eventzilla. |
| [Create Checkout](actions/create-checkout.md) | POST | Creates a checkout in Eventzilla. |
| [Fill Checkout Order](actions/fill-checkout-order.md) | PUT | Updates checkout order details in Eventzilla. |
| [Prepare Checkout](actions/prepare-checkout.md) | GET | Retrieves checkout details for an event date from Eventzilla. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from Eventzilla. |
| [List Events](actions/list-events.md) | GET | Retrieves events from Eventzilla. |
| [Toggle Event Sales](actions/toggle-event-sales.md) | PUT | Updates event sales status in Eventzilla. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Event Order](actions/cancel-event-order.md) | PUT | Cancels an event order in Eventzilla. |
| [Confirm Event Order](actions/confirm-event-order.md) | PUT | Confirms an event order in Eventzilla. |

### Ticket

| Action | Method | Description |
| --- | --- | --- |
| [List Event Tickets](actions/list-event-tickets.md) | GET | Retrieves tickets for an event from Eventzilla. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Get Transaction](actions/get-transaction.md) | GET | Retrieves a transaction from Eventzilla by checkout ID or reference. |
| [List Event Transactions](actions/list-event-transactions.md) | GET | Retrieves transactions for an event from Eventzilla. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Eventzilla. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Eventzilla. |

