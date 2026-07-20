# List Shared Folder Members with Dropbox

Retrieves members of a shared folder from Dropbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/sharing/list_folder_members`
- **Base URL:** `https://api.dropboxapi.com/2`
- **Official documentation:** [List Shared Folder Members](https://www.dropbox.com/developers/documentation/http/documentation#sharing-list_folder_members)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shared_folder_id` | body | `string` | yes | ID of the shared folder to inspect. |
| `limit` | body | `number` | no | Maximum number of members to return. |
| `actions` | body | `list<string>` | no | Optional list of member actions to filter for. Leave blank to return all shared folder members. |
| `cursor` | body | `string` | no | Cursor returned by a previous List Shared Folder Members call. |
