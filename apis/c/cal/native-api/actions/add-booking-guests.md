# Add Booking Guests with Cal.com

Updates a booking in Cal.com by adding guests.

## Endpoint

- **Method:** `POST`
- **Path:** `/bookings/:bookingUid/guests`
- **Base URL:** `https://api.cal.com/v2`
- **Official documentation:** [Add Booking Guests](https://cal.com/docs/api-reference/v2/bookings-guests/add-guests-to-an-existing-booking)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bookingUid` | path | `list` | yes | Booking identifier from Cal.com path parameter. |
| `guests[]` | body | `array<object>` | yes | Array of guest objects to add to the booking. |
| `guests[].email` | body | `string` | yes | Guest email address. |
| `guests[].name` | body | `string` | no | Guest display name. |
| `guests[].timeZone` | body | `string` | no | Guest IANA time zone. |
| `guests[].phoneNumber` | body | `string` | no | Guest phone number. |
| `guests[].language` | body | `string` | no | Guest language code. |
