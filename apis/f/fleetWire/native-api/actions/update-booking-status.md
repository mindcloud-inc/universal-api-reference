# Update Booking Status with FleetWire

Updates an existing booking status in FleetWire.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v2/bookings/:booking_id/status`
- **Base URL:** `https://api.fleetwire.io`
- **Official documentation:** [Update Booking Status](https://documenter.getpostman.com/view/263138/Tz5p6dWS)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `booking_id` | path | `string` | yes | The FleetWire booking identifier. |
| `status` | body | `string` | yes | The new booking status. |
