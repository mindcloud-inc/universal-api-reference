# List Folder Hosts with Checkmk

Retrieves host records from a Checkmk folder.

## Endpoint

- **Method:** `GET`
- **Path:** `/objects/folder_config/{folder}/collections/hosts`
- **Base URL:** `{apiUrl}`
- **Official documentation:** [List Folder Hosts](https://docs.checkmk.com/latest/en/rest_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder` | path | `string` | yes | Folder path or slug, such as ~ for Main or ~linux for the Linux folder. |
