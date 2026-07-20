# Update Page with Notion

Updates an existing page in Notion.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/pages/:page_id`
- **Base URL:** `https://api.notion.com/v1`
- **Official documentation:** [Update Page](https://developers.notion.com/reference/patch-page)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `page_id` | path | `string` | yes |
| `properties` | body | `object` | no |
| `archived` | body | `boolean` | no |
| `in_trash` | body | `boolean` | no |
| `is_locked` | body | `boolean` | no |
| `erase_content` | body | `boolean` | no |
| `icon` | body | `object` | no |
| `cover` | body | `object` | no |
| `template` | body | `object` | no |
| `template.type` | body | `string` | no |
| `template.template_id` | body | `string` | no |
