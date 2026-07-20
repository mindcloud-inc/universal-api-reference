# Update Folder with OpenQR

Updates an existing folder in OpenQR.

## Endpoint

- **Method:** `POST`
- **Path:** `/folders/:folder_id`
- **Base URL:** `https://api.openqr.io/api/v1`
- **Official documentation:** [Update Folder](https://docs.openqr.io/#tag/Folders/operation/UpdateFolder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder_id` | path | `number` | yes | Folder ID. |
| `name` | body | `string` | yes | Folder name. |
