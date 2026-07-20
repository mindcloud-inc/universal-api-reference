# Update Folder with Koncile OCR

## Endpoint

- **Method:** `PUT`
- **Path:** `/update_folder`
- **Base URL:** `https://api.koncile.ai/v1`
- **Official documentation:** [Update Folder](https://docs.koncile.ai/api-setup/folders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `desc` | body | `string` | no | Update the folder description. |
| `folder_id` | query | `number` | yes | The folder identifier to update. |
| `name` | body | `string` | no | Update the folder name. |
