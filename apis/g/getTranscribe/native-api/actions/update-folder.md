# Update Folder with GetTranscribe

Updates a folder in GetTranscribe.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/transcriptions-folders/:id`
- **Base URL:** `https://api.gettranscribe.ai`
- **Official documentation:** [Update Folder](https://www.gettranscribe.ai/api-documentation/folders/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The ID of the folder to update. |
| `name` | body | `string` | no | New name for the folder. |
| `parent_id` | body | `number` | no | New parent folder ID or null for the root. |
