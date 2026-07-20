# Retrieve Page with Notion

Retrieves details for a page from Notion.

## Endpoint

- **Method:** `GET`
- **Path:** `/pages/:page_id`
- **Base URL:** `https://api.notion.com/v1`
- **Official documentation:** [Retrieve Page](https://developers.notion.com/reference/retrieve-a-page)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `page_id` | path | `string` | yes |
| `filter_properties[]` | query | `array<string>` | no |
