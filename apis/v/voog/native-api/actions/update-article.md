# Update Article with Voog

Updates an existing article in the current Voog site.

## Endpoint

- **Method:** `PUT`
- **Path:** `/articles/:articleId`
- **Base URL:** `{siteUrl}/admin/api`
- **Official documentation:** [Update Article](https://www.voog.com/developers/api/resources/articles)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `articleId` | path | `number` | yes | Numeric article ID. |
| `autosaved_title` | body | `string` | yes | Updated draft article title. |
