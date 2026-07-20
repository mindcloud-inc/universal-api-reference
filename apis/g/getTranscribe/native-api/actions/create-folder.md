# Create Folder with GetTranscribe

Creates a folder in GetTranscribe.

## Endpoint

- **Method:** `POST`
- **Path:** `/transcriptions-folders`
- **Base URL:** `https://api.gettranscribe.ai`
- **Official documentation:** [Create Folder](https://www.gettranscribe.ai/api-documentation/folders/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the folder. |
| `parent_id` | body | `number` | no | Optional parent folder ID for subfolders. |
