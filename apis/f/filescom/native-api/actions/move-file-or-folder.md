# Move File or Folder with Files.com

Moves a file or folder within Files.com.

## Endpoint

- **Method:** `POST`
- **Path:** `/file_actions/move/:path`
- **Base URL:** `{siteUrl}/api/rest/v1`
- **Official documentation:** [Move File or Folder](https://developers.files.com/rest/files/files#move-filefolder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | path | `string` | yes | Existing file or folder path to move, without leading or trailing slashes. |
| `destination` | query | `string` | yes | Destination path for the moved file or folder. |
| `overwrite` | query | `boolean` | no | Overwrite the destination if it already exists. |
