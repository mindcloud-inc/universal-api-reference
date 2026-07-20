# Upload file with WorkAdventure

Uploads or replaces a file in WorkAdventure map storage.

## Endpoint

- **Method:** `PUT`
- **Path:** `https://mindcloud-34294.map-storage.workadventu.re/:filePath`
- **Base URL:** `https://admin.workadventu.re`
- **Official documentation:** [Upload file](https://docs.workadventu.re/developer/map-storage-api/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | File content to upload. |
| `filePath` | path | `string` | yes | Stored file path to upload or replace. |
