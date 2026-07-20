# Update Data Source with Notion

## Endpoint

- **Method:** `PATCH`
- **Path:** `/data_sources/:data_source_id`
- **Base URL:** `https://api.notion.com/v1`
- **Official documentation:** [Update Data Source](https://developers.notion.com/reference/update-a-data-source)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Notion-Version` | `2026-03-11` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data_source_id` | path | `string` | yes | ID of a Notion data source. |
| `title[]` | body | `array<object>` | no | Title of the data source as it appears in Notion. |
| `icon` | body | `object` | no | Page icon for the data source. |
| `properties` | body | `object` | no | The property schema of the data source. Keys are property names or IDs, and null values remove properties. |
| `in_trash` | body | `boolean` | no | Whether the data source should be moved to or from the trash. |
| `parent` | body | `object` | no | The parent database to move the data source to. |
