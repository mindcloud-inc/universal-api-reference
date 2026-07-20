# Create Folder with Docsumo

Creates a new folder in Docsumo.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/mew/folder/add/`
- **Base URL:** `https://app.docsumo.com`
- **Official documentation:** [Create Folder](https://support.docsumo.com/reference/folder-creation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder_name` | body | `string` | yes | Name of the folder to create. |
| `type` | body | `string` | yes | Internal document type for the folder, such as invoice. |
