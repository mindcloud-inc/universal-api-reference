# Update Map Layer with Felt

Updates an existing map layer in Felt.

## Endpoint

- **Method:** `POST`
- **Path:** `/maps/:mapId/layers`
- **Base URL:** `https://felt.com/api/v2`
- **Official documentation:** [Update Map Layer](https://developers.felt.com/rest-api/api-reference/layers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mapId` | path | `string` | yes | The ID of the map. |
| `layers[]` | body | `array<object>` | yes | Layer update payloads to apply to the map. |
