# Lodgify: Native API Reference

A consolidated summary of Lodgify's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://docs.lodgify.com/reference
- **API base URL:** `https://api.lodgify.com`

## Authentication

### Custom API Key

Explicit Lodgify API key credential contract for X-ApiKey header auth.

### Credentials

- **API Key:** `apiKey` · required · Your Lodgify API key used for the X-ApiKey request header.

Send these headers with each API request:

```http
X-ApiKey: <apiKey>
```

[Official authentication documentation](https://docs.lodgify.com/docs/authorization)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Booking](actions/get-booking.md) | `GET /v1/reservation/booking/:id` | [docs](https://docs.lodgify.com/reference/getbookingbyid-1) |
| [Get Property](actions/get-property.md) | `GET /v2/properties/:id` | [docs](https://docs.lodgify.com/reference/getpropertybyidv2) |
| [Get Rate Calendar](actions/get-rate-calendar.md) | `GET /v2/rates/calendar` | [docs](https://docs.lodgify.com/reference/ratescalendar-v2) |
| [Get Thread Details](actions/get-thread-details.md) | `GET /v2/messaging/:threadUid` | [docs](https://docs.lodgify.com/reference/get_v2-messaging-threadguid) |
| [List Availability](actions/list-availability.md) | `GET /v2/availability` | [docs](https://docs.lodgify.com/reference/getcalendarbyuser) |
| [List Available Rooms](actions/list-available-rooms.md) | `GET /v2/properties/:id/rooms` | [docs](https://docs.lodgify.com/reference/get_v2-properties-id-rooms) |
| [List Bookings](actions/list-bookings.md) | `GET /v1/reservation` | [docs](https://docs.lodgify.com/reference/bookingslist-1) |
| [List Countries](actions/list-countries.md) | `GET /v1/countries` | [docs](https://docs.lodgify.com/reference/get_v1-countries) |
| [List Currencies](actions/list-currencies.md) | `GET /v1/currencies` | [docs](https://docs.lodgify.com/reference/get_v1-currencies) |
| [List Properties](actions/list-properties.md) | `GET /v2/properties` | [docs](https://docs.lodgify.com/reference/getallpropertiesasync) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks/v1/list` | [docs](https://docs.lodgify.com/reference/get_webhooks-v1-list) |
| [Update Reservation Status](actions/update-reservation-status.md) | `PUT /v1/reservation/booking/:id/:statusAction` | [docs](https://docs.lodgify.com/reference/reservations-2) |
| [Update Room Availability](actions/update-room-availability.md) | `POST /v1/availability/:propertyId/:roomTypeId/set` | [docs](https://docs.lodgify.com/reference/post_v1-availability-propertyid-roomtypeid-set) |
