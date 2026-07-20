# Get Map with Mapulus

Retrieves a specific map from Mapulus.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/maps/:id`
- **Base URL:** `https://api.mapulus.com`
- **Official documentation:** [Get Map](https://developer.mapulus.com/v1/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Map ID. |
| `expand[]` | query | `array<string>` | no | Expand related resources such as layers. |
