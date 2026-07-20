# Delete Folder with Koncile OCR

## Endpoint

- **Method:** `DELETE`
- **Path:** `/delete_folder`
- **Base URL:** `https://api.koncile.ai/v1`
- **Official documentation:** [Delete Folder](https://docs.koncile.ai/api-setup/folders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder_id` | query | `number` | yes | The folder identifier to delete. |
| `override` | query | `boolean` | no | Force deletion when true. |
