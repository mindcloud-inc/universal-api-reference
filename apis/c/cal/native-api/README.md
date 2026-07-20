# Cal.com: Native API Reference

A consolidated summary of Cal.com's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://cal.com/docs/api-reference/v2/introduction
- **OpenAPI specification:** https://cal.com/docs/api-reference/v2/openapi.json
- **API base URL:** `https://api.cal.com/v2`

## Authentication

### OAuth2

Connect your Cal.com account using OAuth2.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://app.cal.com/auth/oauth2/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.cal.com/v2/auth/oauth2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `EVENT_TYPE_READ EVENT_TYPE_WRITE BOOKING_READ BOOKING_WRITE SCHEDULE_READ SCHEDULE_WRITE APPS_READ APPS_WRITE PROFILE_READ PROFILE_WRITE TEAM_MEMBERSHIP_READ TEAM_MEMBERSHIP_WRITE ORG_EVENT_TYPE_READ ORG_EVENT_TYPE_WRITE ORG_BOOKING_READ ORG_BOOKING_WRITE ORG_SCHEDULE_READ ORG_SCHEDULE_WRITE ORG_PROFILE_READ ORG_PROFILE_WRITE`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.cal.com/v2/auth/oauth2/token.

[Official authentication documentation](https://cal.com/docs/api-reference/v2/oauth)

## API conventions

Response data is read from `data`. The total page count is read from `data.pagination.totalPages`. The current page number is read from `data.pagination.currentPage`.

## Pagination

Use `take` in the query string to set the page size (default 25; accepted range 1–250). Use `skip` in the query string as the record offset; numbering starts at 0.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Booking Attendee](actions/add-booking-attendee.md) | `POST /bookings/:bookingUid/attendees` | [docs](https://cal.com/docs/api-reference/v2/bookings-attendees/add-an-attendee-to-a-booking) |
| [Add Booking Guests](actions/add-booking-guests.md) | `POST /bookings/:bookingUid/guests` | [docs](https://cal.com/docs/api-reference/v2/bookings-guests/add-guests-to-an-existing-booking) |
| [Cancel Booking](actions/cancel-booking.md) | `POST /bookings/:bookingUid/cancel` | [docs](https://cal.com/docs/api-reference/v2/bookings/cancel-a-booking) |
| [Confirm Booking](actions/confirm-booking.md) | `POST /bookings/:bookingUid/confirm` | [docs](https://cal.com/docs/api-reference/v2/bookings/confirm-a-booking) |
| [Create Booking](actions/create-booking.md) | `POST /bookings` | [docs](https://cal.com/docs/api-reference/v2/bookings/create-a-booking) |
| [Create Event Type](actions/create-event-type.md) | `POST /event-types` | [docs](https://cal.com/docs/api-reference/v2/event-types/create-an-event-type) |
| [Create Schedule](actions/create-schedule.md) | `POST /schedules` | [docs](https://cal.com/docs/api-reference/v2/schedules/create-a-schedule) |
| [Decline Booking](actions/decline-booking.md) | `POST /bookings/:bookingUid/decline` | [docs](https://cal.com/docs/api-reference/v2/bookings/decline-a-booking) |
| [Delete Event Type](actions/delete-event-type.md) | `DELETE /event-types/:eventTypeId` | [docs](https://cal.com/docs/api-reference/v2/event-types/delete-an-event-type) |
| [Delete Reserved Slot](actions/delete-reserved-slot.md) | `DELETE /slots/reservations/:uid` | [docs](https://cal.com/docs/api-reference/v2/slots/delete-a-reserved-slot) |
| [Delete Schedule](actions/delete-schedule.md) | `DELETE /schedules/:scheduleId` | [docs](https://cal.com/docs/api-reference/v2/schedules/delete-a-schedule) |
| [Get Available Slots](actions/get-available-slots.md) | `GET /slots` | [docs](https://cal.com/docs/api-reference/v2/slots/get-available-time-slots-for-an-event-type) |
| [Get Booking](actions/get-booking.md) | `GET /bookings/:bookingUid` | [docs](https://cal.com/docs/api-reference/v2/bookings/get-a-booking) |
| [Get Event Type](actions/get-event-type.md) | `GET /event-types/:eventTypeId` | [docs](https://cal.com/docs/api-reference/v2/event-types/get-an-event-type) |
| [Get Reserved Slot](actions/get-reserved-slot.md) | `GET /slots/reservations/:uid` | [docs](https://cal.com/docs/api-reference/v2/slots/get-reserved-slot) |
| [Get Schedule](actions/get-schedule.md) | `GET /schedules/:scheduleId` | [docs](https://cal.com/docs/api-reference/v2/schedules/get-a-schedule) |
| [List Bookings](actions/list-bookings.md) | `GET /bookings` | [docs](https://cal.com/docs/api-reference/v2/bookings/get-all-bookings) |
| [List Event Types](actions/list-event-types.md) | `GET /event-types` | [docs](https://cal.com/docs/api-reference/v2/event-types/get-all-event-types) |
| [List Schedules](actions/list-schedules.md) | `GET /schedules` | [docs](https://cal.com/docs/api-reference/v2/schedules/get-all-schedules) |
| [Reschedule Booking](actions/reschedule-booking.md) | `POST /bookings/:bookingUid/reschedule` | [docs](https://cal.com/docs/api-reference/v2/bookings/reschedule-a-booking) |
| [Reserve Slot](actions/reserve-slot.md) | `POST /slots/reservations` | [docs](https://cal.com/docs/api-reference/v2/slots/reserve-a-slot) |
| [Update Booking Location](actions/update-booking-location.md) | `PATCH /bookings/:bookingUid/location` | [docs](https://cal.com/docs/api-reference/v2/bookings/update-booking-location-for-an-existing-booking) |
| [Update Event Type](actions/update-event-type.md) | `PATCH /event-types/:eventTypeId` | [docs](https://cal.com/docs/api-reference/v2/event-types/update-an-event-type) |
| [Update Schedule](actions/update-schedule.md) | `PATCH /schedules/:scheduleId` | [docs](https://cal.com/docs/api-reference/v2/schedules/update-a-schedule) |
