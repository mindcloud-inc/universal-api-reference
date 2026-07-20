# Create Page with Tettra

Creates a new page in Tettra.

## Endpoint

- **Method:** `POST`
- **Path:** `/teams/85329/pages`
- **Base URL:** `https://app.tettra.co/api`
- **Official documentation:** [Create Page](https://support.tettra.com/pages-2/api-endpoint-create-page)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | yes | Page content formatted as HTML. |
| `category_id` | body | `number` | no | Category to publish the page to. |
| `subcategory_id` | body | `number` | no | Subcategory to publish the page to. |
| `title` | body | `string` | yes | Page title. |
