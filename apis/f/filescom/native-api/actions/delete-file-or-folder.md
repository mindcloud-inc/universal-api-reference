# Delete File or Folder with Files.com

Deletes a file or folder from Files.com.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/files/:path`
- **Base URL:** `{siteUrl}/api/rest/v1`
- **Official documentation:** [Delete File or Folder](https://developers.files.com/rest/files/files#delete-filefolder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | path | `string` | yes | File or folder path to delete, without leading or trailing slashes. |
| `recursive` | query | `boolean` | no | Delete folder contents recursively when true. |
