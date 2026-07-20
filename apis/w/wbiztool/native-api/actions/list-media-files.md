# List Media Files with Wbiztool

Retrieves media files from Wbiztool.

## Endpoint

- **Method:** `POST`
- **Path:** `/media/list/`
- **Base URL:** `https://wbiztool.com/api/v1`
- **Official documentation:** [List Media Files](https://wbiztool.com/docs/media-list-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | body | `number` | no | Results page number. |
| `limit` | body | `number` | no | Maximum number of files to return. |
| `file_type` | body | `string` | no | Filter files by type, such as image or document. |
| `search` | body | `string` | no | Search text applied to media file names. |
