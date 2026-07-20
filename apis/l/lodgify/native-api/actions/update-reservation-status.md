# Update Reservation Status with Lodgify

Updates a booking's status in Lodgify.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/reservation/booking/:id/:statusAction`
- **Base URL:** `https://api.lodgify.com`
- **Official documentation:** [Update Reservation Status](https://docs.lodgify.com/reference/reservations-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Reservation identifier from Lodgify. |
| `statusAction` | path | `string` | yes | — |
