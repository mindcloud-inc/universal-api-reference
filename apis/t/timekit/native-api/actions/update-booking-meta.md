# Update Booking Meta with Timekit

Updates metadata for a booking in Timekit.

## Endpoint

- **Method:** `PUT`
- **Path:** `/bookings/:id`
- **Base URL:** `https://api.timekit.io/v2`
- **Official documentation:** [Update Booking Meta](https://developers.timekit.io/reference/update-booking-meta-data)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `meta` | body | `object` | no |
