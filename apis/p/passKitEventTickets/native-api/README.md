# PassKit Event Tickets: Native API Reference

A consolidated summary of PassKit Event Tickets's API configuration and 45 documented operations, with links to official documentation.

- **Official docs:** https://docs.passkit.io/protocols/event-tickets/
- **OpenAPI specification:** https://docs.passkit.io/protocols/event-tickets/eventTickets.swagger.json
- **API base URL:** `https://api.pub2.passkit.io`

## Authentication

### JWT

Generate a signed PassKit JWT from your REST API key and secret for each API request.

[Official authentication documentation](https://help.passkit.com/en/articles/4138220-2-steps-to-call-passkit-api-from-google-app-script)

## Pagination

Use `limit` in the request body to set the page size (default 25; minimum 1). Use `offset` in the request body as the record offset; numbering starts at 0.

## Endpoints (45 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Delete Tickets](actions/bulk-delete-tickets.md) | `DELETE /eventTickets/bulk` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_bulkDeleteTickets) |
| [Copy Production](actions/copy-production.md) | `POST /eventTickets/production/copy` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_copyProduction) |
| [Count Tickets](actions/count-tickets.md) | `POST /eventTickets/tickets/count` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_countTickets) |
| [Create Event](actions/create-event.md) | `POST /eventTickets/event` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_createEvent) |
| [Create Production](actions/create-production.md) | `POST /eventTickets/production` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_createProduction) |
| [Create Ticket](actions/create-ticket.md) | `POST /eventTickets/ticket` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_issueTicket) |
| [Create Ticket By Id](actions/create-ticket-by-id.md) | `POST /eventTickets/ticket/id` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_issueTicketById) |
| [Create Ticket Pass](actions/create-ticket-pass.md) | `POST /eventTickets/pass` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_getEventTicketPass) |
| [Create Ticket Type](actions/create-ticket-type.md) | `POST /eventTickets/ticketType` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_createTicketType) |
| [Create Venue](actions/create-venue.md) | `POST /eventTickets/venue` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_createVenue) |
| [Delete Event](actions/delete-event.md) | `DELETE /eventTickets/event` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_deleteEvent) |
| [Delete Production](actions/delete-production.md) | `DELETE /eventTickets/production` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_deleteProduction) |
| [Delete Ticket](actions/delete-ticket.md) | `DELETE /eventTickets/ticket` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_deleteTicket) |
| [Delete Ticket Type](actions/delete-ticket-type.md) | `DELETE /eventTickets/ticketType` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_deleteTicketType) |
| [Delete Tickets By Order Number](actions/delete-tickets-by-order-number.md) | `DELETE /eventTickets/orderNumber` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_deleteTicketsByOrderNumber) |
| [Delete Venue](actions/delete-venue.md) | `DELETE /eventTickets/venue` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_deleteVenue) |
| [Get Event](actions/get-event.md) | `GET /eventTickets/event/id/:id` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_getEventById) |
| [Get Event Details](actions/get-event-details.md) | `GET /eventTickets/event/details` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_getEventByStartDateAndVenue) |
| [Get Production](actions/get-production.md) | `GET /eventTickets/production/:id` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_getProduction) |
| [Get Production Analytics](actions/get-production-analytics.md) | `GET /eventTickets/production/:classId/analytics` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_getAnalytics) |
| [Get Ticket By Id](actions/get-ticket-by-id.md) | `GET /eventTickets/ticket/id/:id` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_getTicketById) |
| [Get Ticket By Ticket Number](actions/get-ticket-by-ticket-number.md) | `GET /eventTickets/ticket/ticketNumber` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_getTicketByTicketNumber) |
| [Get Ticket Type By Id](actions/get-ticket-type-by-id.md) | `GET /eventTickets/ticketType/id/:id` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_getTicketTypeById) |
| [Get Ticket Type By Uid](actions/get-ticket-type-by-uid.md) | `GET /eventTickets/ticketType/uid/:productionId/:uid` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_getTicketTypeByUserDefinedId) |
| [Get User Profile](actions/get-user-profile.md) | `GET /user/profile` | [docs](https://help.passkit.com/en/articles/4138220-2-steps-to-call-passkit-api-from-google-app-script) |
| [Get Venue](actions/get-venue.md) | `GET /eventTickets/venue/:id` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_getVenueById) |
| [List Events](actions/list-events.md) | `POST /eventTickets/events/list` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_listEvents) |
| [List Productions](actions/list-productions.md) | `POST /eventTickets/productions` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_listProductions) |
| [List Ticket Types](actions/list-ticket-types.md) | `POST /eventTickets/ticketTypes/:productionId` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_listTicketTypes) |
| [List Tickets](actions/list-tickets.md) | `POST /eventTickets/tickets/list` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_listTickets) |
| [List Tickets By Order Number](actions/list-tickets-by-order-number.md) | `GET /eventTickets/tickets/orderNumber` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_getTicketsByOrderNumber) |
| [List Venues](actions/list-venues.md) | `POST /eventTickets/venues` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_listVenues) |
| [Patch Event](actions/patch-event.md) | `PATCH /eventTickets/event` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_patchEvent) |
| [Patch Production](actions/patch-production.md) | `PATCH /eventTickets/production` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_patchProduction) |
| [Patch Ticket Type](actions/patch-ticket-type.md) | `PATCH /eventTickets/ticketType` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_patchTicketType) |
| [Patch Venue](actions/patch-venue.md) | `PATCH /eventTickets/venue` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_patchVenue) |
| [Redeem Ticket](actions/redeem-ticket.md) | `PUT /eventTickets/ticket/redeem` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_redeemTicket) |
| [Redeem Tickets By Order Number](actions/redeem-tickets-by-order-number.md) | `PUT /eventTickets/tickets/orderNumber/redeem` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_redeemTicketsByOrderNumber) |
| [Update Event](actions/update-event.md) | `PUT /eventTickets/event` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_updateEvent) |
| [Update Production](actions/update-production.md) | `PUT /eventTickets/production` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_updateProduction) |
| [Update Ticket](actions/update-ticket.md) | `PUT /eventTickets/ticket` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_updateTicket) |
| [Update Ticket Person](actions/update-ticket-person.md) | `PATCH /eventTickets/ticket/person` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_patchPerson) |
| [Update Ticket Type](actions/update-ticket-type.md) | `PUT /eventTickets/ticketType` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_updateTicketType) |
| [Update Venue](actions/update-venue.md) | `PUT /eventTickets/venue` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_updateVenue) |
| [Validate Ticket](actions/validate-ticket.md) | `PUT /eventTickets/ticket/validate` | [docs](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_validateTicket) |
