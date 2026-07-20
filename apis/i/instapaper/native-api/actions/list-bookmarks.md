# List Bookmarks with Instapaper

## Endpoint

- **Method:** `POST`
- **Path:** `/api/1/bookmarks/list`
- **Base URL:** `https://www.instapaper.com`
- **Official documentation:** [List Bookmarks](https://www.instapaper.com/developers/v1/full-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder_id` | body | `string` | no | Optional folder selector: unread, starred, archive, or a folder ID from List Folders. |
| `have` | body | `string` | no | Optional comma-separated bookmark state list used for sync and progress updates. |
| `highlights` | body | `string` | no | Optional dash-delimited list of highlight IDs the client already has. |
| `limit` | body | `string` | no | Optional number of bookmarks to return, between 1 and 500. Default is 25. |
| `tag` | body | `string` | no | Optional tag filter. Only used when folder_id is not provided. |
