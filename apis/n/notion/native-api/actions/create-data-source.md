# Create Data Source with Notion

## Endpoint

- **Method:** `POST`
- **Path:** `/data_sources`
- **Base URL:** `https://api.notion.com/v1`
- **Official documentation:** [Create Data Source](https://developers.notion.com/reference/create-a-data-source)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Notion-Version` | `2026-03-11` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parent` | body | `object` | yes | An object specifying the parent database of the new data source. |
| `properties` | body | `object` | yes | Property schema of the data source. |
| `title[]` | body | `array<object>` | no | Title of the data source as it appears in Notion. |
| `icon` | body | `object` | no | Page icon for the data source. |
