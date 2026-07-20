# <img src="https://images.mindcloud.co/apps/icons/ticket-source_1774381730670.png" alt="TicketSource logo" width="28" height="28"> TicketSource: Universal API

Manage events, bookings, customers, venues, and ticketing data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ticketSource/latest
- **Category:** Marketing / Events & Webinars
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.ticketsource.co.uk
- **Vendor API docs:** https://reference.ticketsource.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Events](actions/list-events.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketSource/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Booking

| Action | Method | Description |
| --- | --- | --- |
| [Get Booking](actions/get-booking.md) | GET | Retrieves a booking from the TicketSource account. |
| [List Customer Bookings](actions/list-customer-bookings.md) | GET | Retrieves bookings for a customer from TicketSource. |
| [List Date Bookings](actions/list-date-bookings.md) | GET | Retrieves bookings for a date from TicketSource. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in TicketSource. |
| [Delete Customer](actions/delete-customer.md) | DELETE | Deletes an existing customer from TicketSource. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from the TicketSource account. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from the TicketSource account. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in TicketSource. |

### Customer Note

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer Note](actions/create-customer-note.md) | POST | Creates a new customer note in TicketSource. |
| [Delete Customer Note](actions/delete-customer-note.md) | DELETE | Deletes an existing customer note from TicketSource. |
| [Get Customer Note](actions/get-customer-note.md) | GET | Retrieves a customer note from TicketSource. |
| [List Customer Notes](actions/list-customer-notes.md) | GET | Retrieves notes for a customer from TicketSource. |

### Date

| Action | Method | Description |
| --- | --- | --- |
| [Get Date](actions/get-date.md) | GET | Retrieves an event date from TicketSource. |
| [List Event Dates](actions/list-event-dates.md) | GET | Retrieves dates for an event from TicketSource. |
| [List Venue Dates](actions/list-venue-dates.md) | GET | Retrieves dates for a venue from TicketSource. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from the TicketSource account. |
| [List Events](actions/list-events.md) | GET | Retrieves events from the TicketSource account. |

### Seat

| Action | Method | Description |
| --- | --- | --- |
| [Get Seat](actions/get-seat.md) | GET | Retrieves a seat from the TicketSource account. |
| [List Booking Seats](actions/list-booking-seats.md) | GET | Retrieves seats for a booking from TicketSource. |

### Venue

| Action | Method | Description |
| --- | --- | --- |
| [Get Venue](actions/get-venue.md) | GET | Retrieves a venue from the TicketSource account. |
| [List Event Venues](actions/list-event-venues.md) | GET | Retrieves venues for an event from TicketSource. |

