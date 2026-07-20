# Update Booking Location with Cal.com

Updates a booking location in Cal.com.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/bookings/:bookingUid/location`
- **Base URL:** `https://api.cal.com/v2`
- **Official documentation:** [Update Booking Location](https://cal.com/docs/api-reference/v2/bookings/update-booking-location-for-an-existing-booking)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bookingUid` | path | `list` | yes | Booking identifier from Cal.com path parameter. |
| `location` | body | `object` | no | Booking location update payload. |
| `location.type` | body | `string` | no | Location type discriminator. |
| `location.link` | body | `string` | no | Link value for URL-based location types. |
| `location.location` | body | `string` | no | Location value for custom location types. |
| `location.address` | body | `string` | no | Address value for address-based location types. |
| `location.phone` | body | `string` | no | Phone value for phone-based location types. |
