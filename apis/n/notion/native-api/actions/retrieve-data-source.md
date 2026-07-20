# Retrieve Data Source with Notion

Retrieves a data source from Notion.

## Endpoint

- **Method:** `GET`
- **Path:** `/data_sources/:data_source_id`
- **Base URL:** `https://api.notion.com/v1`
- **Official documentation:** [Retrieve Data Source](https://developers.notion.com/reference/retrieve-a-data-source)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Notion-Version` | `2025-09-03` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data_source_id` | path | `string` | yes | ID of the data source. |
