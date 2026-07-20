# Orufy Bookings: Native API Reference

A consolidated summary of Orufy Bookings's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://orufy.com/support/bookings
- **API base URL:** `https://bookings.orufy.com/api/v1/bookings`

## Authentication

### Basic Auth (API Key + Secret)

Connect Orufy Bookings with HTTP Basic auth, using the API Key as the username and the API Secret as the password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://orufy.com/support/bookings/settings/apikeys)

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Booking](actions/cancel-booking.md) | `PATCH /meet/cancel` | [docs](https://orufy.com/support/bookings/bookingsevent) |
| [Create Booking](actions/create-booking.md) | `POST /meet/book` | [docs](https://orufy.com/support/bookings/eventtype/bookinginfo) |
| [Get Booking Queue Status](actions/get-booking-queue-status.md) | `GET /meet/queue-event/status/:queueId` | [docs](https://orufy.com/support/bookings/eventtype/bookinginfo) |
| [Get Event](actions/get-event.md) | `GET /api/event/:eventId` | [docs](https://orufy.com/bookings) |
| [Get Event Availability](actions/get-event-availability.md) | `POST /website/dates` | [docs](https://orufy.com/support/bookings/firstsetup) |
| [Get Public Event](actions/get-public-event.md) | `GET /website/event/:accessLink/:slug` | [docs](https://orufy.com/bookings) |
| [List Events](actions/list-events.md) | `GET /api/event` | [docs](https://orufy.com/bookings) |
| [List Public Events](actions/list-public-events.md) | `GET /website/events/:accessLink` | [docs](https://orufy.com/support/bookings/firstsetup) |
| [Reschedule Booking](actions/reschedule-booking.md) | `PATCH /meet/reschedule` | [docs](https://orufy.com/support/bookings/bookingsevent) |
| [Validate Booking Slot](actions/validate-booking-slot.md) | `POST /meet/slot/validate` | [docs](https://orufy.com/support/bookings/firstsetup) |
