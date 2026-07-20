# Move File or Folder with Dropbox

Moves a file or folder in Dropbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/files/move_v2`
- **Base URL:** `https://api.dropboxapi.com/2`
- **Official documentation:** [Move File or Folder](https://www.dropbox.com/developers/documentation/http/documentation#files-move_v2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_path` | body | `string` | yes | Source Dropbox path to move. |
| `to_path` | body | `string` | yes | Destination Dropbox path after the move. |
| `autorename` | body | `boolean` | no | Automatically rename the moved item on conflict. |
| `allow_ownership_transfer` | body | `boolean` | no | Allow Dropbox to transfer ownership when needed. |
