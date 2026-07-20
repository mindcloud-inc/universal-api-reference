# Delete Folder with Checkmk

Deletes an existing folder from Checkmk.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/objects/folder_config/{folder}`
- **Base URL:** `{apiUrl}`
- **Official documentation:** [Delete Folder](https://docs.checkmk.com/latest/en/rest_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder` | path | `string` | yes | Folder path or slug to delete. |
