# Create Article with Voog

Creates a new article in the current Voog site.

## Endpoint

- **Method:** `POST`
- **Path:** `/articles`
- **Base URL:** `{siteUrl}/admin/api`
- **Official documentation:** [Create Article](https://www.voog.com/developers/api/resources/articles)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `autosaved_title` | body | `string` | yes | Draft article title. |
| `page_id` | body | `number` | yes | Parent blog page ID. |
