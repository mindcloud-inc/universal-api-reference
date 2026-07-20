# Copy map file with WorkAdventure

Copies a file in WorkAdventure map storage.

## Endpoint

- **Method:** `POST`
- **Path:** `https://mindcloud-34294.map-storage.workadventu.re/copy`
- **Base URL:** `https://admin.workadventu.re`
- **Official documentation:** [Copy map file](https://github.com/workadventure/workadventure/tree/develop/map-storage)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source` | body | `string` | yes | Existing map-storage file path to copy from. |
| `destination` | body | `string` | yes | New map-storage file path to copy to. |
