# List Folder Children with Wrike

Finds child folders in a Wrike folder.

## Endpoint

- **Method:** `GET`
- **Path:** `/folders/:folderId/folders`
- **Base URL:** `https://{host}/api/v4`
- **Official documentation:** [List Folder Children](https://developers.wrike.com/api/v4/folders-projects/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | path | `string` | yes | Wrike parent folder ID. |
