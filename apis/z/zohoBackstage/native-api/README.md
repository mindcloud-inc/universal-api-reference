# Zoho Backstage: Native API Reference

A consolidated summary of Zoho Backstage's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://www.zoho.com/backstage/api/v3/introduction.html
- **API base URL:** `https://zohoapis.com/backstage`

## Authentication

### OAuth 2.0

Connect Zoho Backstage with a Zoho OAuth 2.0 client and authorize the required Zoho Backstage scopes.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.zoho.com/oauth/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://accounts.zoho.com/oauth/v2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `zohobackstage.portal.READ zohobackstage.event.READ zohobackstage.event.CREATE zohobackstage.event.UPDATE zohobackstage.event.DELETE zohobackstage.speaker.READ zohobackstage.speaker.CREATE zohobackstage.speaker.UPDATE zohobackstage.speaker.DELETE zohobackstage.sponsor.READ zohobackstage.sponsor.CREATE zohobackstage.sponsor.UPDATE zohobackstage.sponsor.DELETE zohobackstage.eventticket.READ zohobackstage.eventticket.CREATE zohobackstage.eventticket.UPDATE zohobackstage.eventticket.DELETE zohobackstage.order.READ zohobackstage.order.CREATE zohobackstage.order.UPDATE zohobackstage.order.DELETE zohobackstage.attendee.READ zohobackstage.attendee.UPDATE zohobackstage.attendee.DELETE zohobackstage.agenda.READ zohobackstage.agenda.CREATE zohobackstage.agenda.UPDATE zohobackstage.agenda.DELETE zohobackstage.webhook.READ zohobackstage.webhook.CREATE zohobackstage.webhook.UPDATE zohobackstage.webhook.DELETE zohobackstage.exhibitor.READ zohobackstage.exhibitor.CREATE zohobackstage.exhibitor.UPDATE zohobackstage.exhibitor.DELETE`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://accounts.zoho.com/oauth/v2/token.

[Official authentication documentation](https://www.zoho.com/backstage/api/v3/oauth.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

The total page count is read from `pagination.total_pages`. The current page number is read from `pagination.page`.

## Pagination

Use `per_page` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Agenda](actions/create-agenda.md) | `POST /v3/portals/:portal_id/events/:event_id/agendas` | [docs](https://www.zoho.com/backstage/api/v3/create-an-agenda.html) |
| [Create Event](actions/create-event.md) | `POST /v3/portals/:portal_id/events` | [docs](https://www.zoho.com/backstage/api/v3/create-an-event.html) |
| [Create Event Webhook](actions/create-event-webhook.md) | `POST /v3/portals/:portal_id/events/:event_id/webhooks` | [docs](https://www.zoho.com/backstage/api/v3/create-a-webhook-for-event.html) |
| [Create Portal Webhook](actions/create-portal-webhook.md) | `POST /v3/portals/:portal_id/webhooks` | [docs](https://www.zoho.com/backstage/api/v3/create-a-webhook-for-portal.html) |
| [Create Session](actions/create-session.md) | `POST /v3/portals/:portal_id/events/:event_id/sessions` | [docs](https://www.zoho.com/backstage/api/v3/create-a-session.html) |
| [Create Speaker](actions/create-speaker.md) | `POST /v3/portals/:portal_id/events/:event_id/speakers` | [docs](https://www.zoho.com/backstage/api/v3/create-a-speaker.html) |
| [Delete Event](actions/delete-event.md) | `DELETE /v3/portals/:portal_id/events/:event_id` | [docs](https://www.zoho.com/backstage/api/v3/delete-an-event.html) |
| [List Agendas](actions/list-agendas.md) | `GET /v3/portals/:portal_id/events/:event_id/agendas` | [docs](https://www.zoho.com/backstage/api/v3/get-all-agendas.html) |
| [List Attendees](actions/list-attendees.md) | `GET /v3/portals/:portal_id/events/:event_id/attendees` | [docs](https://www.zoho.com/backstage/api/v3/get-all-attendees.html) |
| [List Event Members](actions/list-event-members.md) | `GET /v3/portals/:portal_id/events/:event_id/members` | [docs](https://www.zoho.com/backstage/api/v3/get-all-event-members.html) |
| [List Events](actions/list-events.md) | `GET /v3/portals/:portal_id/events` | [docs](https://www.zoho.com/backstage/api/v3/get-all-events.html) |
| [List Exhibitors](actions/list-exhibitors.md) | `GET /v3/portals/:portal_id/events/:event_id/exhibitors` | [docs](https://www.zoho.com/backstage/api/v3/get-all-exhibitors.html) |
| [List Orders](actions/list-orders.md) | `GET /v3/portals/:portal_id/events/:event_id/orders` | [docs](https://www.zoho.com/backstage/api/v3/get-all-orders.html) |
| [List Portal Members](actions/list-portal-members.md) | `GET /v3/portals/:portal_id/members` | [docs](https://www.zoho.com/backstage/api/v3/get-all-portal-members.html) |
| [List Portals](actions/list-portals.md) | `GET /v3/portals` | [docs](https://www.zoho.com/backstage/api/v3/get-all-portals.html) |
| [List Sessions](actions/list-sessions.md) | `GET /v3/portals/:portal_id/events/:event_id/sessions` | [docs](https://www.zoho.com/backstage/api/v3/get-all-sessions.html) |
| [List Speakers](actions/list-speakers.md) | `GET /v3/portals/:portal_id/events/:event_id/speakers` | [docs](https://www.zoho.com/backstage/api/v3/get-all-speakers.html) |
| [List Sponsors](actions/list-sponsors.md) | `GET /v3/portals/:portal_id/events/:event_id/sponsors` | [docs](https://www.zoho.com/backstage/api/v3/get-all-sponsors.html) |
| [List Ticket Classes](actions/list-ticket-classes.md) | `GET /v3/portals/:portal_id/events/:event_id/ticket_classes` | [docs](https://www.zoho.com/backstage/api/v3/get-all-ticket-classes.html) |
