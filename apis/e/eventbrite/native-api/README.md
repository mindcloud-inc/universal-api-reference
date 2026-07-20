# Eventbrite: Native API Reference

A consolidated summary of Eventbrite's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://www.eventbrite.com/platform/api
- **API base URL:** `https://www.eventbriteapi.com/v3`

## Authentication

### OAuth2

OAuth2 authorization code flow for Eventbrite API access.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://www.eventbrite.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://www.eventbrite.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


[Official authentication documentation](https://www.eventbrite.com/platform/api)

### API Key

Bearer token authentication for Eventbrite API private tokens and legacy Nvite tenant keys.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.eventbrite.com/platform/api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `pagination.continuation`. The total page count is read from `pagination.page_count`. The current page number is read from `pagination.page_number`.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Copy Event](actions/copy-event.md) | `POST /events/:eventId/copy/` | [docs](https://www.eventbrite.com/platform/docs/create-events) |
| [Create Event Ticket Class](actions/create-event-ticket-class.md) | `POST /events/:eventId/ticket_classes/` | [docs](https://www.eventbrite.com/platform/docs/create-events) |
| [Create Organization Event](actions/create-organization-event.md) | `POST /organizations/:organizationId/events/` | [docs](https://www.eventbrite.com/platform/api#/reference/event/create/create-an-event) |
| [Create Organization Organizer](actions/create-organization-organizer.md) | `POST /organizations/:organizationId/organizers/` | [docs](https://www.eventbrite.com/platform/docs/organizations) |
| [Create Organization Venue](actions/create-organization-venue.md) | `POST /organizations/:organizationId/venues/` | [docs](https://www.eventbrite.com/platform/api#/reference/venue/create/create-a-venue) |
| [Delete Event](actions/delete-event.md) | `DELETE /events/:eventId/` | [docs](https://www.eventbrite.com/platform/api) |
| [Get Attendee](actions/get-attendee.md) | `GET /attendees/:attendeeId/` | [docs](https://www.eventbrite.com/platform/docs/attendees) |
| [Get Current User](actions/get-current-user.md) | `GET /users/me/` | [docs](https://www.eventbrite.com/platform/docs/api-explorer) |
| [Get Event](actions/get-event.md) | `GET /events/:eventId/` | [docs](https://www.eventbrite.com/platform/api#/reference/event/retrieve-an-event) |
| [Get Order](actions/get-order.md) | `GET /orders/:orderId/` | [docs](https://www.eventbrite.com/platform/docs/order-lookup) |
| [Get Organization Attendees Report](actions/get-organization-attendees-report.md) | `GET /organizations/:organizationId/reports/attendees/` |  |
| [Get Organization Sales Report](actions/get-organization-sales-report.md) | `GET /organizations/:organizationId/reports/sales/` |  |
| [Get Organizer](actions/get-organizer.md) | `GET /organizers/:organizerId/` | [docs](https://www.eventbrite.com/platform/api) |
| [Get Venue](actions/get-venue.md) | `GET /venues/:venueId/` | [docs](https://www.eventbrite.com/platform/api) |
| [List Event Attendees](actions/list-event-attendees.md) | `GET /events/:eventId/attendees/` | [docs](https://www.eventbrite.com/platform/docs/attendees) |
| [List Event Orders](actions/list-event-orders.md) | `GET /events/:eventId/orders/` | [docs](https://www.eventbrite.com/platform/docs/orders) |
| [List Event Ticket Classes](actions/list-event-ticket-classes.md) | `GET /events/:eventId/ticket_classes/` | [docs](https://www.eventbrite.com/platform/docs/create-events) |
| [List My Organizations](actions/list-my-organizations.md) | `GET /users/me/organizations/` | [docs](https://www.eventbrite.com/platform/api#/reference/organization/list-your-organizations/list-your-organizations) |
| [List Organization Attendees](actions/list-organization-attendees.md) | `GET /organizations/:organizationId/attendees/` | [docs](https://www.eventbrite.com/platform/api#/reference/attendee/list/list-attendees-by-organization) |
| [List Organization Events](actions/list-organization-events.md) | `GET /organizations/:organizationId/events/` | [docs](https://www.eventbrite.com/platform/api#/reference/event/list/list-events-by-organization) |
| [List Organization Orders](actions/list-organization-orders.md) | `GET /organizations/:organizationId/orders/` | [docs](https://www.eventbrite.com/platform/api#/reference/order/organization-orders/list-orders-by-organization) |
| [List Organization Organizers](actions/list-organization-organizers.md) | `GET /organizations/:organizationId/organizers/` | [docs](https://www.eventbrite.com/platform/docs/organizations) |
| [List Organization Venues](actions/list-organization-venues.md) | `GET /organizations/:organizationId/venues/` | [docs](https://www.eventbrite.com/platform/api#/reference/venue/list/list-venues-by-organization) |
| [List Organizer Events](actions/list-organizer-events.md) | `GET /organizers/:organizerId/events/` | [docs](https://www.eventbrite.com/platform/api) |
| [List Venue Events](actions/list-venue-events.md) | `GET /venues/:venueId/events/` | [docs](https://www.eventbrite.com/platform/api#/reference/event/list/list-events-by-venue) |
| [Publish Event](actions/publish-event.md) | `POST /events/:eventId/publish/` | [docs](https://www.eventbrite.com/platform/docs/create-events) |
| [Unpublish Event](actions/unpublish-event.md) | `POST /events/:eventId/unpublish/` | [docs](https://www.eventbrite.com/platform/docs/create-events) |
| [Update Event](actions/update-event.md) | `POST /events/:eventId/` | [docs](https://www.eventbrite.com/platform/docs/create-events) |
| [Update Organizer](actions/update-organizer.md) | `POST /organizers/:organizerId/` | [docs](https://www.eventbrite.com/platform/api) |
| [Update Venue](actions/update-venue.md) | `POST /venues/:venueId/` | [docs](https://www.eventbrite.com/platform/api) |
