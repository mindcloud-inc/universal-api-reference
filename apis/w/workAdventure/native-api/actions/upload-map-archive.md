# Upload map archive with WorkAdventure

Uploads a ZIP archive to WorkAdventure map storage.

## Endpoint

- **Method:** `POST`
- **Path:** `https://mindcloud-34294.map-storage.workadventu.re/upload`
- **Base URL:** `https://admin.workadventu.re`
- **Official documentation:** [Upload map archive](https://docs.workadventu.re/developer/map-storage-api/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | ZIP archive containing map-storage files to upload. |
| `directory` | body | `string` | no | Optional target directory inside map storage. |
