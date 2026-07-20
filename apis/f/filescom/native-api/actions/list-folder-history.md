# List Folder History with Files.com

Retrieves history for a folder from Files.com.

## Endpoint

- **Method:** `GET`
- **Path:** `/history/folders/:path`
- **Base URL:** `{siteUrl}/api/rest/v1`
- **Official documentation:** [List Folder History](https://developers.files.com/rest/resources/logging/actions/#list-history-for-specific-folder)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cursor` | query | `string` | no | Cursor token returned by a previous history response page. |
| `display` | query | `string` | no | Optional display mode. Files.com supports `full` or `parent`. |
| `end_at` | query | `date` | no | Return history entries at or before this timestamp. |
| `path` | path | `string` | yes | Folder path without leading or trailing slashes. |
| `per_page` | query | `number` | no | Maximum number of history entries to return in one page. |
| `start_at` | query | `date` | no | Return history entries at or after this timestamp. |
