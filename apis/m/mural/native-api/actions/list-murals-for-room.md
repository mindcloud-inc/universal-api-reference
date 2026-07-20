# List Murals for Room with Mural

Finds murals in Mural for a room.

## Endpoint

- **Method:** `GET`
- **Path:** `/rooms/:roomId/murals`
- **Base URL:** `https://app.mural.co/api/public/v1`
- **Official documentation:** [List Murals for Room](https://developers.mural.co/public/reference/getroommurals)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | query | `string` | no | Filter murals by their corresponding folder. |
| `roomId` | path | `number` | yes | Unique identifier of a room. |
| `sortBy` | query | `string` | no | Sort murals by the documented Mural sort order. |
| `status` | query | `string` | no | Filter murals by active or archived status. |
