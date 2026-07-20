# Update Room Type with Channex

Updates a room type in Channex.

## Endpoint

- **Method:** `PUT`
- **Path:** `/room_types/:id`
- **Base URL:** `https://staging.channex.io/api/v1`
- **Official documentation:** [Update Room Type](https://docs.channex.io/api-v.1-documentation/room-types-collection#update-room-type)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | UUID of the room type to update. |
| `room_type` | body | `object` | yes | Top-level room_type payload object documented by Channex for room type updates. |
