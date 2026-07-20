# Delete Room Type with Channex

Deletes a room type from Channex.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/room_types/:id`
- **Base URL:** `https://staging.channex.io/api/v1`
- **Official documentation:** [Delete Room Type](https://docs.channex.io/api-v.1-documentation/room-types-collection#remove-room-type)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | UUID of the room type to delete. |
| `force` | query | `boolean` | no | Set true to force removal when supported by Channex. |
