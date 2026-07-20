# Update Booking State with Timekit

Updates a booking's state in Timekit.

## Endpoint

- **Method:** `PUT`
- **Path:** `/bookings/:id/:action`
- **Base URL:** `https://api.timekit.io/v2`
- **Official documentation:** [Update Booking State](https://developers.timekit.io/reference/bookingsidaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action` | path | `list<string>` | yes | Accepted values: `cancel`, `cancel_by_customer`, `complete`, `confirm`, `decline`. |
| `apply_to_bulked_bookings` | body | `boolean` | no | — |
| `id` | path | `string` | yes | — |
