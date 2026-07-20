# List Shared Links with Dropbox

Retrieves shared links for the current user from Dropbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/sharing/list_shared_links`
- **Base URL:** `https://api.dropboxapi.com/2`
- **Official documentation:** [List Shared Links](https://www.dropbox.com/developers/documentation/http/documentation#sharing-list_shared_links)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | body | `string` | no | Path to a file or folder. When omitted, Dropbox returns the current user's shared links. |
| `direct_only` | body | `boolean` | no | When true, return only links directly on the path instead of inherited links. |
| `cursor` | body | `string` | no | Cursor returned by a previous List Shared Links call. |
