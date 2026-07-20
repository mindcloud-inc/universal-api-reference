# List Data Source Templates with Notion

Retrieves page templates for a Notion data source.

## Endpoint

- **Method:** `GET`
- **Path:** `/data_sources/:data_source_id/templates`
- **Base URL:** `https://api.notion.com/v1`
- **Official documentation:** [List Data Source Templates](https://developers.notion.com/reference/list-data-source-templates)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Notion-Version` | `2025-09-03` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data_source_id` | path | `string` | yes | ID of the data source. |
| `name` | query | `string` | no | Filter templates by name. |
| `start_cursor` | query | `string` | no | Cursor for pagination. |
| `page_size` | query | `number` | no | Maximum number of templates per page (max 100). |
