# Update Page with Siteleaf

Updates an existing page in Siteleaf.

## Endpoint

- **Method:** `PUT`
- **Path:** `/pages/:page_id`
- **Base URL:** `https://api.siteleaf.com/v2`
- **Official documentation:** [Update Page](https://learn.siteleaf.com/api/pages/#update-a-page)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page_id` | path | `string` | no | Siteleaf page identifier |
| `title` | body | `string` | no | Updated page title |
