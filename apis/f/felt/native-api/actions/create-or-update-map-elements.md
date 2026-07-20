# Create Or Update Map Elements with Felt

Creates or updates map elements in Felt.

## Endpoint

- **Method:** `POST`
- **Path:** `/maps/:mapId/elements`
- **Base URL:** `https://felt.com/api/v2`
- **Official documentation:** [Create Or Update Map Elements](https://developers.felt.com/rest-api/api-reference/elements)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mapId` | path | `string` | yes | The ID of the map to create the elements in. |
| `features[]` | body | `array<object>` | yes | GeoJSON features to create or update. |
