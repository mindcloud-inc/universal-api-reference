# Create Booking with Makeplans

Creates a new booking in Makeplans.

## Endpoint

- **Method:** `POST`
- **Path:** `/bookings`
- **Base URL:** `https://{accountDomain}/api/v1`
- **Official documentation:** [Create Booking](https://developer.makeplans.com/endpoints/bookings/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `booking.resource_id` | body | `number` | yes | Required Makeplans resource ID. |
| `booking.title` | body | `string` | no | Optional booking title. |
| `booking.booked_from` | body | `date` | yes | Booking start datetime. |
| `booking.booked_to` | body | `date` | yes | Booking end datetime. |
| `booking.service_id` | body | `number` | no | Optional service ID. |
| `booking.person_id` | body | `number` | no | Optional person ID. |
