# Query Data Source with Notion

Retrieves filtered records from a Notion data source.

## Endpoint

- **Method:** `POST`
- **Path:** `/data_sources/:data_source_id/query`
- **Base URL:** `https://api.notion.com/v1`
- **Official documentation:** [Query Data Source](https://developers.notion.com/reference/query-a-data-source)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Notion-Version` | `2025-09-03` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data_source_id` | path | `string` | yes | ID of the data source. |
| `filter` | body | `object` | no | Filter conditions for the query body. |
| `filter_properties` | body | `list<string>` | no | Property IDs used to limit filter formula computation. |
| `result_type` | body | `string` | no | Limit results to a specific object type. |
| `sorts` | body | `list<object>` | no | Sort definitions for query results. |
| `start_cursor` | body | `string` | no | Cursor for pagination. |
| `page_size` | body | `number` | no | Maximum number of results per page (max 100). |
| `archived` | body | `boolean` | no | Include archived pages in query results. |
| `in_trash` | body | `boolean` | no | Include pages currently in trash. |
