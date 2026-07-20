# Create Database with Notion

## Endpoint

- **Method:** `POST`
- **Path:** `/databases`
- **Base URL:** `https://api.notion.com/v1`
- **Official documentation:** [Create Database](https://developers.notion.com/reference/create-database)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Notion-Version` | `2026-03-11` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parent` | body | `object` | yes | The parent page or workspace where the database will be created. |
| `title[]` | body | `array<object>` | no | The title of the database as a Notion rich text array. |
| `description[]` | body | `array<object>` | no | The description of the database as a Notion rich text array. |
| `is_inline` | body | `boolean` | no | Whether the database should be displayed inline in the parent page. |
| `initial_data_source` | body | `object` | no | Initial data source configuration for the database, including its properties schema. |
| `icon` | body | `object` | no | The icon for the database. |
| `cover` | body | `object` | no | The cover image for the database. |
