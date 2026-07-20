# Create Page with Notion

Creates a new page in Notion.

## Endpoint

- **Method:** `POST`
- **Path:** `/pages`
- **Base URL:** `https://api.notion.com/v1`
- **Official documentation:** [Create Page](https://developers.notion.com/reference/post-page)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `parent` | body | `object` | no |
| `parent.page_id` | body | `string` | no |
| `parent.database_id` | body | `string` | no |
| `parent.data_source_id` | body | `string` | no |
| `parent.workspace` | body | `boolean` | no |
| `properties` | body | `object` | no |
| `children[]` | body | `array<object>` | no |
| `content[]` | body | `array<object>` | no |
| `markdown` | body | `string` | no |
| `icon` | body | `object` | no |
| `cover` | body | `object` | no |
| `template` | body | `object` | no |
| `template.type` | body | `string` | no |
| `template.template_id` | body | `string` | no |
| `position` | body | `object` | no |
| `position.type` | body | `string` | no |
| `position.after_block.id` | body | `string` | no |
