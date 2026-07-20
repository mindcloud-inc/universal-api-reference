# Update Database with Notion

## Endpoint

- **Method:** `PATCH`
- **Path:** `/databases/:database_id`
- **Base URL:** `https://api.notion.com/v1`
- **Official documentation:** [Update Database](https://developers.notion.com/reference/update-database)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Notion-Version` | `2026-03-11` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `database_id` | path | `string` | yes | ID of a Notion database, a container for one or more data sources. |
| `parent` | body | `object` | no | The parent page or workspace to move the database to. |
| `title[]` | body | `array<object>` | no | The updated title of the database as a Notion rich text array. |
| `description[]` | body | `array<object>` | no | The updated description of the database as a Notion rich text array. |
| `is_inline` | body | `boolean` | no | Whether the database should be displayed inline in the parent page. |
| `icon` | body | `object` | no | The updated icon for the database. |
| `cover` | body | `object` | no | The updated cover image for the database. |
| `in_trash` | body | `boolean` | no | Whether the database should be moved to or from the trash. |
| `is_locked` | body | `boolean` | no | Whether the database should be locked from editing in the Notion app UI. |
