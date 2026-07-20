# Get File Download Link with Files.com

Retrieves a file download link from Files.com.

## Endpoint

- **Method:** `GET`
- **Path:** `/files/:path`
- **Base URL:** `{siteUrl}/api/rest/v1`
- **Official documentation:** [Get File Download Link](https://developers.files.com/rest/files/files#download-file-optimized)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | path | `string` | yes | File path without leading or trailing slashes. |
