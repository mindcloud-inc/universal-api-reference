# Update Page with Tettra

Updates an existing page in Tettra.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/teams/85329/pages/:page_id`
- **Base URL:** `https://app.tettra.co/api`
- **Official documentation:** [Update Page](https://support.tettra.com/pages-2/api-endpoint-update-page)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | no | Replacement page content formatted as HTML. |
| `category_id` | body | `number` | no | Updated category ID. |
| `owner_id` | body | `number` | no | Updated owner of the page. |
| `page_id` | path | `number` | yes | Page ID to update. |
| `subcategory_id` | body | `number` | no | Updated subcategory ID. |
| `title` | body | `string` | no | Updated page title. |
