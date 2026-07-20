# AddCal: Native API Reference

A consolidated summary of AddCal's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://addcal.co/api-docs
- **OpenAPI specification:** https://addcal.co/docs.openapi
- **API base URL:** `https://addcal.co/api`

## Authentication

### API Token

Use your AddCal API token as a Bearer token for API requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://addcal.co/docs)

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Calendar](actions/create-calendar.md) | `POST /calendars` | [docs](https://addcal.co/api-docs) |
| [Create Calendar Event](actions/create-calendar-event.md) | `POST /calendars/:calendar_public_id/events` | [docs](https://addcal.co/api-docs) |
| [Create Event](actions/create-event.md) | `POST /events` | [docs](https://addcal.co/api-docs) |
| [Create Event RSVP](actions/create-event-rsvp.md) | `POST /calendars/:calendar_public_id/events/:event_public_id/rsvps` | [docs](https://addcal.co/api-docs) |
| [Delete Calendar](actions/delete-calendar.md) | `DELETE /calendars/:public_id` | [docs](https://addcal.co/api-docs) |
| [Delete Calendar Event](actions/delete-calendar-event.md) | `DELETE /calendars/:calendar_public_id/events/:public_id` | [docs](https://addcal.co/api-docs) |
| [Delete Event RSVP](actions/delete-event-rsvp.md) | `DELETE /calendars/:calendar_public_id/events/:event_public_id/rsvps/:public_id` | [docs](https://addcal.co/api-docs) |
| [Get Calendar](actions/get-calendar.md) | `GET /calendars/:calendar_id` | [docs](https://addcal.co/api-docs) |
| [Get Calendar Event](actions/get-calendar-event.md) | `GET /calendars/:calendar_public_id/events/:public_id` | [docs](https://addcal.co/api-docs) |
| [Get Current User](actions/get-current-user.md) | `GET /users/me` | [docs](https://addcal.co/api-docs) |
| [Get Event RSVP](actions/get-event-rsvp.md) | `GET /calendars/:calendar_public_id/events/:event_public_id/rsvps/:public_id` | [docs](https://addcal.co/api-docs) |
| [List Calendar Events](actions/list-calendar-events.md) | `GET /calendars/:calendar_public_id/events` | [docs](https://addcal.co/api-docs) |
| [List Calendars](actions/list-calendars.md) | `GET /calendars` | [docs](https://addcal.co/api-docs) |
| [List Event RSVPs](actions/list-event-rsvps.md) | `GET /calendars/:calendar_public_id/events/:event_public_id/rsvps` | [docs](https://addcal.co/api-docs) |
| [List Events](actions/list-events.md) | `GET /events` | [docs](https://addcal.co/api-docs) |
| [Update Calendar](actions/update-calendar.md) | `PUT /calendars/:public_id` | [docs](https://addcal.co/api-docs) |
| [Update Calendar Event](actions/update-calendar-event.md) | `PUT /calendars/:calendar_public_id/events/:public_id` | [docs](https://addcal.co/api-docs) |
| [Update Event RSVP](actions/update-event-rsvp.md) | `PUT /calendars/:calendar_public_id/events/:event_public_id/rsvps/:public_id` | [docs](https://addcal.co/api-docs) |
