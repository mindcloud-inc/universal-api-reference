# Create Folder with Canva

Creates a new folder in Canva.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/folders`
- **Base URL:** `https://api.canva.com/rest`
- **Official documentation:** [Create Folder](https://www.canva.dev/docs/connect/api-reference/folders/create-folder/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the folder. Maximum length: 255. |
| `parent_folder_id` | body | `string` | yes | The folder ID of the parent folder. Use root for top-level projects or uploads for the Uploads folder. Maximum length: 50. |
