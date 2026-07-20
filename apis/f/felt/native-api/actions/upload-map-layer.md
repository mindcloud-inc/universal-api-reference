# Upload Map Layer with Felt

Uploads a new map layer to Felt.

## Endpoint

- **Method:** `POST`
- **Path:** `/maps/:mapId/upload`
- **Base URL:** `https://felt.com/api/v2`
- **Official documentation:** [Upload Map Layer](https://developers.felt.com/rest-api/api-reference/layers/layer-uploads)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mapId` | path | `string` | yes | Map ID to upload the new layer to. |
| `name` | body | `string` | yes | Display name for the new layer. |
| `import_url` | body | `string` | no | Public URL to geodata to import instead of uploading a file. |
| `metadata` | body | `object` | no | Optional layer metadata object. |
