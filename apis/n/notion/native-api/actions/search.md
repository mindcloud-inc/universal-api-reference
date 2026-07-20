# Search with Notion

Finds pages and data sources in Notion by title.

## Endpoint

- **Method:** `POST`
- **Path:** `/search`
- **Base URL:** `https://api.notion.com/v1`
- **Official documentation:** [Search](https://developers.notion.com/reference/post-search)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Notion-Version` | `2025-09-03` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | no | Text to search for in titles and content. |
| `filter.property` | body | `list` | no | Property type to filter by. Accepted values: `0`. |
| `filter.value` | body | `list` | no | Object value to filter search results. Accepted values: `0`, `1`. |
| `sort.direction` | body | `list` | no | Sort direction for result ordering. Accepted values: `0`, `1`. |
| `sort.timestamp` | body | `list` | no | Timestamp field used for sorting. Accepted values: `0`. |
| `page_size` | body | `number` | no | Number of results to return (max 100). |
| `start_cursor` | body | `string` | no | Pagination cursor returned by previous response. |
