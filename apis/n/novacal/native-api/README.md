# Novacal: Native API Reference

A consolidated summary of Novacal's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://docs.novacal.io/
- **API base URL:** `https://api.novacal.io`

## Authentication

### API Key

Novacal API key sent as a Bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.novacal.io/api-reference/introduction)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Book Event](actions/book-event.md) | `POST /v1/events` | [docs](https://docs.novacal.io/api-reference/v1/events/create) |
| [Cancel Event](actions/cancel-event.md) | `PUT /v1/events/:id/cancel` | [docs](https://docs.novacal.io/api-reference/v1/events/cancel) |
| [Create Booking Form Field](actions/create-booking-form-field.md) | `POST /v1/event-types/:eventType/booking-forms` | [docs](https://docs.novacal.io/api-reference/v1/booking-forms/create) |
| [Create Event Type](actions/create-event-type.md) | `POST /v1/event-types` | [docs](https://docs.novacal.io/api-reference/v1/event-types/create) |
| [Delete Booking Form Field](actions/delete-booking-form-field.md) | `DELETE /v1/event-types/:eventType/booking-forms/:field` | [docs](https://docs.novacal.io/api-reference/v1/booking-forms/delete) |
| [Delete Event Type](actions/delete-event-type.md) | `DELETE /v1/event-types/:id` | [docs](https://docs.novacal.io/api-reference/v1/event-types/delete) |
| [Get Availability](actions/get-availability.md) | `GET /v1/availability` | [docs](https://docs.novacal.io/api-reference/v1/availability/get) |
| [Get Current User](actions/get-current-user.md) | `GET /v1/users/me` | [docs](https://docs.novacal.io/api-reference/v1/users/me) |
| [Get Event](actions/get-event.md) | `GET /v1/events/:id` | [docs](https://docs.novacal.io/api-reference/v1/events/find) |
| [Get Event Type](actions/get-event-type.md) | `GET /v1/event-types/:id` | [docs](https://docs.novacal.io/api-reference/v1/event-types/find) |
| [Get Team](actions/get-team.md) | `GET /v1/teams/:id` | [docs](https://docs.novacal.io/api-reference/v1/teams/find) |
| [List Booking Form Fields](actions/list-booking-form-fields.md) | `GET /v1/event-types/:eventType/booking-forms` | [docs](https://docs.novacal.io/api-reference/v1/booking-forms/get) |
| [List Event Types](actions/list-event-types.md) | `GET /v1/event-types` | [docs](https://docs.novacal.io/api-reference/v1/event-types/get) |
| [List Events](actions/list-events.md) | `GET /v1/events` | [docs](https://docs.novacal.io/api-reference/v1/events/get) |
| [List Teams](actions/list-teams.md) | `GET /v1/teams` | [docs](https://docs.novacal.io/api-reference/v1/teams/get) |
| [Reschedule Event](actions/reschedule-event.md) | `PUT /v1/events/:id` | [docs](https://docs.novacal.io/api-reference/v1/events/update) |
| [Update Booking Form Field](actions/update-booking-form-field.md) | `PUT /v1/event-types/:eventType/booking-forms/:field` | [docs](https://docs.novacal.io/api-reference/v1/booking-forms/update) |
| [Update Booking Form Field Order](actions/update-booking-form-field-order.md) | `PUT /v1/event-types/:eventType/booking-forms/update-order` | [docs](https://docs.novacal.io/api-reference/v1/booking-forms/update-order) |
| [Update Current User](actions/update-current-user.md) | `PUT /v1/users/me` | [docs](https://docs.novacal.io/api-reference/v1/users/update-me) |
| [Update Event Type](actions/update-event-type.md) | `PUT /v1/event-types/:id` | [docs](https://docs.novacal.io/api-reference/v1/event-types/update) |
