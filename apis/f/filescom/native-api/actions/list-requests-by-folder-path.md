# List Requests by Folder Path with Files.com

Retrieves requests for a folder path from Files.com.

## Endpoint

- **Method:** `GET`
- **Path:** `/requests/folders/:path`
- **Base URL:** `{siteUrl}/api/rest/v1`
- **Official documentation:** [List Requests by Folder Path](https://developers.files.com/rest/resources/file-system/requests/#list-requests)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mine` | query | `boolean` | no | When true, return only requests owned by the current Files.com user. |
| `path` | path | `string` | yes | Folder path without leading or trailing slashes. |
