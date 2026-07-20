# Get Map Layer with Felt

Retrieves a map layer from Felt.

## Endpoint

- **Method:** `GET`
- **Path:** `/maps/:mapId/layers/:layerId`
- **Base URL:** `https://felt.com/api/v2`
- **Official documentation:** [Get Map Layer](https://developers.felt.com/rest-api/api-reference/layers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mapId` | path | `string` | yes | The Felt map ID. |
| `layerId` | path | `string` | yes | The Felt layer ID. |
