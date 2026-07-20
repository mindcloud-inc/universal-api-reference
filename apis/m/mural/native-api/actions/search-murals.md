# Search Murals with Mural

Finds murals in Mural by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/search/:workspaceId/murals`
- **Base URL:** `https://app.mural.co/api/public/v1`
- **Official documentation:** [Search Murals](https://developers.mural.co/public/reference/searchmurals)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | The text this search query is for. |
| `workspaceId` | path | `string` | yes | Unique identifier of a workspace. |
