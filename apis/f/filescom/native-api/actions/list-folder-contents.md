# List Folder Contents with Files.com

Retrieves folder contents by path from Files.com.

## Endpoint

- **Method:** `GET`
- **Path:** `/folders/:path`
- **Base URL:** `{siteUrl}/api/rest/v1`
- **Official documentation:** [List Folder Contents](https://developers.files.com/rest/files/files#list-folders-by-path)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modified_at_datetime` | query | `date` | no | Return only items modified after this timestamp. Use only together with Type. |
| `path` | path | `string` | no | Folder path without leading or trailing slashes. Leave blank to list the Files.com site root. |
| `search_custom_metadata_key` | query | `string` | no | When Search is set, restrict the search to a specific custom metadata key, or use `*` to match any key. |
| `search` | query | `string` | no | Search for items by name within the selected folder. |
| `search_all` | query | `boolean` | no | Search the entire Files.com site when true. Do not send Path at the same time. |
| `type` | query | `string` | no | Limit results to `file` or `folder` items. |
| `per_page` | query | `number` | no | Maximum number of entries to return in one page. |
| `cursor` | query | `string` | no | Cursor token returned by a previous folder-list response page. |
