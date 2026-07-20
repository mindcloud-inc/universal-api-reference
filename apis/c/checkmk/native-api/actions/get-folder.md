# Get Folder with Checkmk

Retrieves folder configuration details from Checkmk.

## Endpoint

- **Method:** `GET`
- **Path:** `/objects/folder_config/{folder}`
- **Base URL:** `{apiUrl}`
- **Official documentation:** [Get Folder](https://docs.checkmk.com/latest/en/rest_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder` | path | `string` | yes | Folder path or slug, such as ~ for Main or ~linux for the Linux folder. |
