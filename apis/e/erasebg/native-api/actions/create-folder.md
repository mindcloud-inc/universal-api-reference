# Create Folder with Erase.bg

Creates a folder in Erase.bg storage.

## Endpoint

- **Method:** `POST`
- **Path:** `/service/platform/assets/v1.0/folders`
- **Base URL:** `https://api.pixelbin.io`
- **Official documentation:** [Create Folder](https://www.pixelbin.io/docs/storage/create-folder/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the folder to create. |
| `path` | body | `string` | no | Parent path where the folder should be created. |
