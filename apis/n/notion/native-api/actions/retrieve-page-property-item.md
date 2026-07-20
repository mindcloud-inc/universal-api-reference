# Retrieve Page Property Item with Notion

Retrieves a page property item from Notion.

## Endpoint

- **Method:** `GET`
- **Path:** `/pages/:page_id/properties/:property_id`
- **Base URL:** `https://api.notion.com/v1`
- **Official documentation:** [Retrieve Page Property Item](https://developers.notion.com/reference/retrieve-a-page-property)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `page_id` | path | `string` | yes |
| `property_id` | path | `string` | yes |
| `start_cursor` | query | `string` | no |
| `page_size` | query | `number` | no |
