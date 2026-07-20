# List File Comments with Files.com

Retrieves file comments by path from Files.com.

## Endpoint

- **Method:** `GET`
- **Path:** `/file_comments/files/:path`
- **Base URL:** `{siteUrl}/api/rest/v1`
- **Official documentation:** [List File Comments](https://developers.files.com/rest/resources/file-system/file-comments#list-file-comments-by-path)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | path | `string` | yes | File or folder path without leading or trailing slashes. |
