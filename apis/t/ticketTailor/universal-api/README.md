# <img src="https://images.mindcloud.co/apps/icons/images_1773251500651.png" alt="Ticket Tailor logo" width="28" height="28"> Ticket Tailor: Universal API

Sell tickets, manage events, and track orders with Ticket Tailor

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ticketTailor/latest
- **Category:** Marketing / Events & Webinars
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.tickettailor.com/
- **Vendor API docs:** https://developers.tickettailor.com/docs/intro/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Events](actions/list-events.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Check In

| Action | Method | Description |
| --- | --- | --- |
| [List Check Ins](actions/list-check-ins.md) | GET | Retrieves box office check-ins from Ticket Tailor. |

### Checkout Form

| Action | Method | Description |
| --- | --- | --- |
| [List Checkout Forms](actions/list-checkout-forms.md) | GET | Retrieves checkout forms from Ticket Tailor. |

### Checkout Form Element

| Action | Method | Description |
| --- | --- | --- |
| [Get Checkout Form Element](actions/get-checkout-form-element.md) | GET | Retrieves a checkout form element from Ticket Tailor. |
| [List Checkout Form Elements](actions/list-checkout-form-elements.md) | GET | Retrieves checkout form elements from Ticket Tailor. |

### Discount

| Action | Method | Description |
| --- | --- | --- |
| [Get Discount](actions/get-discount.md) | GET | Retrieves a discount from Ticket Tailor. |
| [List Discounts](actions/list-discounts.md) | GET | Retrieves discounts from Ticket Tailor. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from Ticket Tailor. |
| [List Events](actions/list-events.md) | GET | Retrieves box office events from Ticket Tailor. |

### Event Occurrence

| Action | Method | Description |
| --- | --- | --- |
| [Get Event Occurrence](actions/get-event-occurrence.md) | GET | Retrieves an event occurrence from Ticket Tailor. |
| [List Event Occurrences](actions/list-event-occurrences.md) | GET | Retrieves event occurrences for a Ticket Tailor event series. |

### Event Series

| Action | Method | Description |
| --- | --- | --- |
| [Get Event Series](actions/get-event-series.md) | GET | Retrieves an event series from Ticket Tailor. |
| [List Event Series](actions/list-event-series.md) | GET | Retrieves box office event series from Ticket Tailor. |

### Hold

| Action | Method | Description |
| --- | --- | --- |
| [Get Hold](actions/get-hold.md) | GET | Retrieves a hold from Ticket Tailor. |
| [List Holds](actions/list-holds.md) | GET | Retrieves holds from Ticket Tailor. |

### Issued Ticket

| Action | Method | Description |
| --- | --- | --- |
| [Get Issued Ticket](actions/get-issued-ticket.md) | GET | Retrieves an issued ticket from Ticket Tailor. |
| [List Issued Tickets](actions/list-issued-tickets.md) | GET | Retrieves issued tickets from Ticket Tailor. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from Ticket Tailor. |
| [List Orders](actions/list-orders.md) | GET | Retrieves box office orders from Ticket Tailor. |

### Overview

| Action | Method | Description |
| --- | --- | --- |
| [Get Overview](actions/get-overview.md) | GET | Retrieves box office overview statistics from Ticket Tailor. |

### Ping

| Action | Method | Description |
| --- | --- | --- |
| [Ping](actions/ping.md) | GET | Checks if the Ticket Tailor API is responsive. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from Ticket Tailor. |
| [List Products](actions/list-products.md) | GET | Retrieves products from Ticket Tailor. |

### Store

| Action | Method | Description |
| --- | --- | --- |
| [Get Store](actions/get-store.md) | GET | Retrieves store information from Ticket Tailor. |
| [List Stores](actions/list-stores.md) | GET | Retrieves stores from Ticket Tailor. |

