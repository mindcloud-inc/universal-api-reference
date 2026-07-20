# Move Map with Felt

Moves a map to another location in Felt.

## Endpoint

- **Method:** `POST`
- **Path:** `/maps/:mapId/move`
- **Base URL:** `https://felt.com/api/v2`
- **Official documentation:** [Move Map](https://developers.felt.com/rest-api/api-reference/maps)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mapId` | path | `string` | yes | The Felt map ID. |
| `project_id` | body | `string` | no | Destination project ID. |
| `folder_id` | body | `string` | no | Destination folder ID. |
