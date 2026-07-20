# Search Rooms with Mural

Finds rooms in Mural by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/search/:workspaceId/rooms`
- **Base URL:** `https://app.mural.co/api/public/v1`
- **Official documentation:** [Search Rooms](https://developers.mural.co/public/reference/searchrooms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | The text this search query is for. |
| `workspaceId` | path | `string` | yes | Unique identifier of a workspace. |
