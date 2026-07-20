# Get File or Folder Metadata with Files.com

Finds a file or folder in Files.com by path.

## Endpoint

- **Method:** `GET`
- **Path:** `/file_actions/metadata/:path`
- **Base URL:** `{siteUrl}/api/rest/v1`
- **Official documentation:** [Get File or Folder Metadata](https://developers.files.com/rest/files/files#find-filefolder-by-path)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | path | `string` | yes | File or folder path without leading or trailing slashes. |
