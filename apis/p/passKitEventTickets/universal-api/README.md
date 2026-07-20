# <img src="https://images.mindcloud.co/apps/icons/pass-kit-event-tickets_1775502030035.png" alt="PassKit Event Tickets logo" width="28" height="28"> PassKit Event Tickets: Universal API

PassKit Event Tickets lets teams create, manage, validate, redeem, and analyze PassKit event productions, venues, ticket types, events, and tickets through PassKit's Event Ticketing APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/passKitEventTickets/latest
- **Actions:** 45
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://passkit.com
- **Vendor API docs:** https://docs.passkit.io/protocols/event-tickets/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Profile](actions/get-user-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/passKitEventTickets/latest/actions/get-user-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (45)

### Custom Objects

| Action | Method | Description |
| --- | --- | --- |
| [Copy Production](actions/copy-production.md) | POST | Creates a copy of a production in PassKit. |
| [Create Production](actions/create-production.md) | POST | Creates a new production in PassKit. |
| [Delete Production](actions/delete-production.md) | DELETE | Deletes an existing production from PassKit. |
| [Get Production](actions/get-production.md) | GET | Retrieves production details from PassKit. |
| [List Productions](actions/list-productions.md) | GET | Retrieves productions from PassKit. |
| [Patch Production](actions/patch-production.md) | PUT | Partially updates an existing production in PassKit. |
| [Update Production](actions/update-production.md) | PUT | Fully updates an existing production in PassKit. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | POST | Creates a new event in PassKit. |
| [Delete Event](actions/delete-event.md) | DELETE | Deletes an existing event from PassKit. |
| [Get Event](actions/get-event.md) | GET | Retrieves event details from PassKit. |
| [Get Event Details](actions/get-event-details.md) | GET | Retrieves an event by start date and venue from PassKit. |
| [List Events](actions/list-events.md) | GET | Retrieves events for a production from PassKit. |
| [Patch Event](actions/patch-event.md) | PUT | Partially updates an existing event in PassKit. |
| [Update Event](actions/update-event.md) | PUT | Fully updates an existing event in PassKit. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Create Venue](actions/create-venue.md) | POST | Creates a new venue in PassKit. |
| [Delete Venue](actions/delete-venue.md) | DELETE | Deletes an existing venue from PassKit. |
| [Get Venue](actions/get-venue.md) | GET | Retrieves venue details from PassKit. |
| [List Venues](actions/list-venues.md) | GET | Retrieves venues from PassKit. |
| [Patch Venue](actions/patch-venue.md) | PUT | Partially updates an existing venue in PassKit. |
| [Update Venue](actions/update-venue.md) | PUT | Fully updates an existing venue in PassKit. |

### Production Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Production Analytics](actions/get-production-analytics.md) | GET | Retrieves production analytics from PassKit. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Count Tickets](actions/count-tickets.md) | GET | Retrieves a filtered ticket count from PassKit. |

### Tickets

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Delete Tickets](actions/bulk-delete-tickets.md) | DELETE | Deletes multiple tickets from PassKit. |
| [Create Ticket](actions/create-ticket.md) | POST | Creates a new ticket in PassKit. |
| [Create Ticket By Id](actions/create-ticket-by-id.md) | POST | Creates a new ticket in PassKit by user-defined IDs. |
| [Create Ticket Pass](actions/create-ticket-pass.md) | POST | Retrieves event ticket passes from PassKit. |
| [Create Ticket Type](actions/create-ticket-type.md) | POST | Creates a new ticket type in PassKit. |
| [Delete Ticket](actions/delete-ticket.md) | DELETE | Deletes an existing ticket from PassKit. |
| [Delete Ticket Type](actions/delete-ticket-type.md) | DELETE | Deletes an existing ticket type from PassKit. |
| [Delete Tickets By Order Number](actions/delete-tickets-by-order-number.md) | DELETE | Deletes tickets by order number from PassKit. |
| [Get Ticket By Id](actions/get-ticket-by-id.md) | GET | Retrieves a ticket by ID from PassKit. |
| [Get Ticket By Ticket Number](actions/get-ticket-by-ticket-number.md) | GET | Retrieves a ticket by ticket number from PassKit. |
| [Get Ticket Type By Id](actions/get-ticket-type-by-id.md) | GET | Retrieves a ticket type by ID from PassKit. |
| [Get Ticket Type By Uid](actions/get-ticket-type-by-uid.md) | GET | Retrieves a ticket type by user-defined ID from PassKit. |
| [List Ticket Types](actions/list-ticket-types.md) | GET | Retrieves ticket types from PassKit. |
| [List Tickets](actions/list-tickets.md) | GET | Retrieves tickets for a production from PassKit. |
| [List Tickets By Order Number](actions/list-tickets-by-order-number.md) | GET | Retrieves tickets by order number from PassKit. |
| [Patch Ticket Type](actions/patch-ticket-type.md) | PUT | Partially updates an existing ticket type in PassKit. |
| [Redeem Ticket](actions/redeem-ticket.md) | PUT | Redeems an existing ticket in PassKit. |
| [Redeem Tickets By Order Number](actions/redeem-tickets-by-order-number.md) | PUT | Redeems tickets by order number in PassKit. |
| [Update Ticket](actions/update-ticket.md) | PUT | Updates an existing ticket in PassKit. |
| [Update Ticket Person](actions/update-ticket-person.md) | PUT | Updates ticket holder information in PassKit. |
| [Update Ticket Type](actions/update-ticket-type.md) | PUT | Updates an existing ticket type in PassKit. |
| [Validate Ticket](actions/validate-ticket.md) | PUT | Validates an existing ticket in PassKit. |

### User Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get User Profile](actions/get-user-profile.md) | GET | Retrieves your user profile from PassKit. |

