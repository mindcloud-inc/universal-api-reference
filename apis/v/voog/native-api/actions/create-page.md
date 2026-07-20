# Create Page with Voog

Creates a new page in the current Voog site.

## Endpoint

- **Method:** `POST`
- **Path:** `/pages`
- **Base URL:** `{siteUrl}/admin/api`
- **Official documentation:** [Create Page](https://www.voog.com/developers/api/resources/pages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `layout_id` | body | `number` | yes | Layout ID for the new page. |
| `parent_id` | body | `number` | yes | Parent page ID for the new page. |
| `title` | body | `string` | yes | Page title shown in the menu. |
