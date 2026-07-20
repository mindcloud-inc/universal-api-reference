# Update Map with Felt

Updates an existing map in Felt.

## Endpoint

- **Method:** `POST`
- **Path:** `/maps/:mapId/update`
- **Base URL:** `https://felt.com/api/v2`
- **Official documentation:** [Update Map](https://developers.felt.com/rest-api/api-reference/maps)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mapId` | path | `string` | yes | The Felt map ID. |
| `title` | body | `string` | no | The new map title. |
| `description` | body | `string` | no | A description shown in the map legend. |
| `public_access` | body | `string` | no | Map sharing level. |
| `basemap` | body | `string` | no | Basemap style or raster tile URL. |
