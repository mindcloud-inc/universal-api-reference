# List Folder Tasks with Wrike

Finds tasks in a Wrike folder.

## Endpoint

- **Method:** `GET`
- **Path:** `/folders/:folderId/tasks`
- **Base URL:** `https://{host}/api/v4`
- **Official documentation:** [List Folder Tasks](https://developers.wrike.com/api/v4/tasks/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | path | `string` | yes | Wrike folder ID. |
