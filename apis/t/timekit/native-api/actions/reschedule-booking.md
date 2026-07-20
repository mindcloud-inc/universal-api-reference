# Reschedule Booking with Timekit

## Endpoint

- **Method:** `POST`
- **Path:** `/bookings/:id/reschedule`
- **Base URL:** `https://api.timekit.io/v2`
- **Official documentation:** [Reschedule Booking](https://developers.timekit.io/reference/reschedule-a-booking)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `end` | body | `string` | yes |
| `id` | path | `string` | yes |
| `resource_id` | body | `string` | yes |
| `start` | body | `string` | yes |
