# Update Booking with Flexopus

Updates an existing booking in Flexopus.

## Endpoint

- **Method:** `PUT`
- **Path:** `/bookings/:id`
- **Base URL:** `{tenantBaseUrl}/api/v1`
- **Official documentation:** [Update Booking](https://flexopus.com/api/docs/#endpoints-PUTapi-v1-bookings--id-)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the booking. |
| `from_time` | body | `date` | no | When the booking will start. |
| `to_time` | body | `date` | yes | When the booking will end. |
| `user_vehicle_id` | body | `number` | no | Vehicle ID when reserving a parking space. |
