# Upsert Room with Liveblocks

Updates a room in Liveblocks, or creates it if missing.

## Endpoint

- **Method:** `POST`
- **Path:** `/rooms/:roomId/upsert`
- **Base URL:** `https://api.liveblocks.io/v2`
- **Official documentation:** [Upsert Room](https://liveblocks.io/docs/api-reference/rest-api-endpoints#upsert-update-or-create-room)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `roomId` | path | `string` | no | ID of the room. |
