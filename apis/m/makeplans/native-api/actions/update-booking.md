# Update Booking with Makeplans

Updates an existing booking in Makeplans.

## Endpoint

- **Method:** `PUT`
- **Path:** `/bookings/:bookingId`
- **Base URL:** `https://{accountDomain}/api/v1`
- **Official documentation:** [Update Booking](https://developer.makeplans.com/endpoints/bookings/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `booking.booked_from` | body | `date` | no | Booking start datetime. |
| `booking.booked_to` | body | `date` | no | Booking end datetime. |
| `booking.resource_id` | body | `number` | no | Makeplans resource ID for the booking. |
| `booking.title` | body | `string` | no | Optional booking title. |
| `bookingId` | path | `number` | yes | The Makeplans booking ID. |
