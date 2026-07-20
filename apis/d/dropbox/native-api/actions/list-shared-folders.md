# List Shared Folders with Dropbox

Retrieves shared folders for the current user from Dropbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/sharing/list_folders`
- **Base URL:** `https://api.dropboxapi.com/2`
- **Official documentation:** [List Shared Folders](https://www.dropbox.com/developers/documentation/http/documentation#sharing-list_folders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | body | `number` | no | Maximum number of shared folders to return. |
| `actions` | body | `list<string>` | no | Optional list of folder actions to filter for. Leave blank to return all shared folders. |
