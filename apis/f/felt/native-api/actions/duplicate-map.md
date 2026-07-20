# Duplicate Map with Felt

Creates a duplicate of a map in Felt.

## Endpoint

- **Method:** `POST`
- **Path:** `/maps/:mapId/duplicate`
- **Base URL:** `https://felt.com/api/v2`
- **Official documentation:** [Duplicate Map](https://developers.felt.com/rest-api/api-reference/maps)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mapId` | path | `string` | yes | The Felt map ID. |
| `title` | body | `string` | no | Title for the duplicated map. |
| `destination` | body | `object` | no | Destination object with either project_id or folder_id. |
