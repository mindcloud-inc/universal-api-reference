# Create Booking with Flexopus

Creates a new booking in Flexopus.

## Endpoint

- **Method:** `POST`
- **Path:** `/bookings`
- **Base URL:** `{tenantBaseUrl}/api/v1`
- **Official documentation:** [Create Booking](https://flexopus.com/api/docs/#endpoints-POSTapi-v1-bookings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bookable_id` | body | `number` | yes | ID of the bookable to reserve. |
| `from_time` | body | `date` | no | When the booking will start. |
| `to_time` | body | `date` | yes | When the booking will end. |
| `user_id` | body | `number` | yes | ID of the user for whom the reservation is made. |
| `location_id` | body | `number` | yes | ID of the location for the reservation. |
| `guest_email` | body | `string` | no | Guest email address for a guest booking. |
| `guest_name` | body | `string` | no | Guest name for a guest booking. |
| `booking_info` | body | `string` | no | Purpose of the booking for a guest booking. |
| `user_vehicle_id` | body | `number` | no | Vehicle ID when reserving a parking space. |
