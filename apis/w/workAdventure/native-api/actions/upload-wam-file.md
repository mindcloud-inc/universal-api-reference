# Upload WAM file with WorkAdventure

Uploads or replaces a WAM file in WorkAdventure map storage.

## Endpoint

- **Method:** `PUT`
- **Path:** `https://mindcloud-34294.map-storage.workadventu.re/:wamPath`
- **Base URL:** `https://admin.workadventu.re`
- **Official documentation:** [Upload WAM file](https://github.com/workadventure/workadventure/tree/develop/map-storage)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `wamPath` | path | `string` | yes | Destination WAM file path, including the .wam suffix. |
| `file` | body | `file` | yes | URL, base64, or binary content for the WAM file upload. |
