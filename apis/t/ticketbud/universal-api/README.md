# <img src="https://images.mindcloud.co/apps/icons/ticketbud_1774964762810.png" alt="Ticketbud logo" width="28" height="28"> Ticketbud: Universal API

Ticketbud: Create events, sell tickets, and manage attendees

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ticketbud/latest
- **Category:** Marketing / Events & Webinars
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.ticketbud.com/
- **Vendor API docs:** https://api.ticketbud.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketbud/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from Ticketbud. |
| [Get Event Sales Summary](actions/get-event-sales-summary.md) | GET | Retrieves an event sales summary from Ticketbud. |
| [Get Event Totals](actions/get-event-totals.md) | GET | Retrieves event totals from Ticketbud. |
| [List Events](actions/list-events.md) | GET | Retrieves events from Ticketbud. |

### Ticket

| Action | Method | Description |
| --- | --- | --- |
| [Check In Ticket](actions/check-in-ticket.md) | PUT | Checks in a ticket in Ticketbud. |
| [Get Ticket By Barcode](actions/get-ticket-by-barcode.md) | GET | Finds a ticket in Ticketbud by barcode. |
| [Get Ticket By ID](actions/get-ticket-by-id.md) | GET | Retrieves a ticket from Ticketbud by ID. |
| [Get Ticket Sales By Type](actions/get-ticket-sales-by-type.md) | GET | Retrieves ticket sales by ticket type from Ticketbud. |
| [List Event Tickets](actions/list-event-tickets.md) | GET | Retrieves event tickets from Ticketbud. |
| [Undo Ticket Check In](actions/undo-ticket-check-in.md) | PUT | Reverses a ticket check-in in Ticketbud. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Ticketbud. |

