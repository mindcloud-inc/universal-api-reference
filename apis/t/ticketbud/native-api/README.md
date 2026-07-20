# Ticketbud: Native API Reference

A consolidated summary of Ticketbud's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://api.ticketbud.com/
- **API base URL:** `https://api.ticketbud.com`

## Authentication

### OAuth2

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://api.ticketbud.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.ticketbud.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `events`.

Refresh expired access tokens with a POST request to https://api.ticketbud.com/oauth/token.

[Official authentication documentation](https://api.ticketbud.com/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check In Ticket](actions/check-in-ticket.md) | `PUT /events/:eventId/tickets/:id/check_in.json` | [docs](https://api.ticketbud.com/) |
| [Get Current User](actions/get-current-user.md) | `GET /me.json` | [docs](https://api.ticketbud.com/) |
| [Get Event](actions/get-event.md) | `GET /events/:id.json` | [docs](https://api.ticketbud.com/) |
| [Get Event Sales Summary](actions/get-event-sales-summary.md) | `GET /events/:eventId/ticket_sales` | [docs](https://api.ticketbud.com/) |
| [Get Event Totals](actions/get-event-totals.md) | `GET /events/:id/totals.json` | [docs](https://api.ticketbud.com/) |
| [Get Ticket By Barcode](actions/get-ticket-by-barcode.md) | `GET /events/:eventId/tickets/:barcode.json` | [docs](https://api.ticketbud.com/) |
| [Get Ticket By ID](actions/get-ticket-by-id.md) | `GET /events/:eventId/tickets/:id.json` | [docs](https://api.ticketbud.com/) |
| [Get Ticket Sales By Type](actions/get-ticket-sales-by-type.md) | `GET /events/:eventId/ticket_sales/:id.json` | [docs](https://api.ticketbud.com/) |
| [List Event Tickets](actions/list-event-tickets.md) | `GET /events/:eventId/tickets.json` | [docs](https://api.ticketbud.com/) |
| [List Events](actions/list-events.md) | `GET /events.json` | [docs](https://api.ticketbud.com/) |
| [Undo Ticket Check In](actions/undo-ticket-check-in.md) | `PUT /events/:eventId/tickets/:id/check_in.json` | [docs](https://api.ticketbud.com/) |
