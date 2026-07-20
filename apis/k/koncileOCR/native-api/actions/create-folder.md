# Create Folder with Koncile OCR

## Endpoint

- **Method:** `POST`
- **Path:** `/create_folder`
- **Base URL:** `https://api.koncile.ai/v1`
- **Official documentation:** [Create Folder](https://docs.koncile.ai/api-setup/folders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `desc` | body | `string` | no | A detailed description of the folder. |
| `name` | body | `string` | yes | The folder name to create. |
