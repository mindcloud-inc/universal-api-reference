# Copy File or Folder with Files.com

Copies a file or folder within Files.com.

## Endpoint

- **Method:** `POST`
- **Path:** `/file_actions/copy/:path`
- **Base URL:** `{siteUrl}/api/rest/v1`
- **Official documentation:** [Copy File or Folder](https://developers.files.com/rest/files/files#copy-filefolder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | path | `string` | yes | Existing file or folder path to copy, without leading or trailing slashes. |
| `destination` | query | `string` | yes | Destination path for the copied file or folder. |
| `overwrite` | query | `boolean` | no | Overwrite the destination if it already exists. |
| `copy_behaviors` | query | `boolean` | no | Copy permissions and related behaviors where supported. |
| `structure` | query | `boolean` | no | Preserve structure semantics during the copy when supported. |
