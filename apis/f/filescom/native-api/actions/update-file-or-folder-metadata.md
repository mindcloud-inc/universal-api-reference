# Update File or Folder Metadata with Files.com

Updates file or folder metadata in Files.com.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/files/:path`
- **Base URL:** `{siteUrl}/api/rest/v1`
- **Official documentation:** [Update File or Folder Metadata](https://developers.files.com/rest/files/files#update-filefolder-metadata)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | path | `string` | yes | Existing file or folder path to update, without leading or trailing slashes. |
| `custom_metadata` | body | `object` | no | JSON object of custom metadata fields to store on the file or folder. |
| `priority_color` | body | `string` | no | Priority color label to apply. |
