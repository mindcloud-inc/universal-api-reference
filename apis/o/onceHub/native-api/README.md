# OnceHub: Native API Reference

A consolidated summary of OnceHub's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://developers.oncehub.com/api-reference/
- **API base URL:** `https://api.oncehub.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.oncehub.com/docs/overview/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–100). Use `after` in the query string as the pagination cursor.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Booking](actions/cancel-booking.md) | `POST /v2/bookings/:id/cancel` | [docs](https://developers.oncehub.com/reference/booking-calendars/) |
| [Create Booking Calendar One-Time Link](actions/create-booking-calendar-one-time-link.md) | `POST /v2/booking-calendars/:id/one-time-links` | [docs](https://developers.oncehub.com/reference/booking-calendars/) |
| [Create Webhook](actions/create-webhook.md) | `POST /v1/webhooks` | [docs](https://developers.oncehub.com/reference/oncehub-v1/) |
| [Get Booking](actions/get-booking.md) | `GET /v2/bookings/:id` | [docs](https://developers.oncehub.com/reference/booking-calendars/) |
| [Get Booking Calendar](actions/get-booking-calendar.md) | `GET /v2/booking-calendars/:id` | [docs](https://developers.oncehub.com/reference/booking-calendars/) |
| [Get Contact](actions/get-contact.md) | `GET /v2/contacts/:id` | [docs](https://developers.oncehub.com/reference/booking-calendars/) |
| [Get Team](actions/get-team.md) | `GET /v2/teams/:id` | [docs](https://developers.oncehub.com/reference/booking-calendars/) |
| [Get User](actions/get-user.md) | `GET /v2/users/:id` | [docs](https://developers.oncehub.com/reference/booking-calendars/) |
| [Get Webhook](actions/get-webhook.md) | `GET /v2/webhooks/:id` | [docs](https://developers.oncehub.com/reference/booking-calendars/) |
| [List Booking Calendars](actions/list-booking-calendars.md) | `GET /v2/booking-calendars` | [docs](https://developers.oncehub.com/reference/booking-calendars/) |
| [List Booking Pages](actions/list-booking-pages.md) | `GET /v2/booking-pages` | [docs](https://developers.oncehub.com/reference/booking-pages/) |
| [List Bookings](actions/list-bookings.md) | `GET /v2/bookings` | [docs](https://developers.oncehub.com/reference/booking-calendars/) |
| [List Contacts](actions/list-contacts.md) | `GET /v2/contacts` | [docs](https://developers.oncehub.com/reference/booking-calendars/) |
| [List Event Types](actions/list-event-types.md) | `GET /v2/event-types` | [docs](https://developers.oncehub.com/reference/booking-pages/) |
| [List Master Pages](actions/list-master-pages.md) | `GET /v2/master-pages` | [docs](https://developers.oncehub.com/reference/booking-pages/) |
| [List Teams](actions/list-teams.md) | `GET /v2/teams` | [docs](https://developers.oncehub.com/reference/booking-calendars/) |
| [List Users](actions/list-users.md) | `GET /v2/users` | [docs](https://developers.oncehub.com/reference/booking-calendars/) |
| [List Webhooks](actions/list-webhooks.md) | `GET /v1/webhooks` | [docs](https://developers.oncehub.com/reference/oncehub-v1/) |
| [Request Booking Reschedule](actions/request-booking-reschedule.md) | `POST /v2/bookings/:id/request-reschedule` | [docs](https://developers.oncehub.com/reference/booking-calendars/) |
| [Set Booking No-Show](actions/set-booking-no-show.md) | `POST /v2/bookings/:id/no-show` | [docs](https://developers.oncehub.com/reference/booking-calendars/) |
| [Validate API Key](actions/validate-api-key.md) | `GET /v1/test` | [docs](https://developers.oncehub.com/reference/oncehub-v1/) |
