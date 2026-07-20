# List Folders for Room with Mural

Finds folders in Mural for a room.

## Endpoint

- **Method:** `GET`
- **Path:** `/rooms/:roomId/folders`
- **Base URL:** `https://app.mural.co/api/public/v1`
- **Official documentation:** [List Folders for Room](https://developers.mural.co/public/reference/getroomfolders)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `roomId` | path | `number` | yes | Unique identifier of a room. |
