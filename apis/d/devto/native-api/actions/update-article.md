# Update Article with Dev.to

Updates an existing Dev.to article by ID.

## Endpoint

- **Method:** `PUT`
- **Path:** `/articles/:id`
- **Base URL:** `https://dev.to/api`
- **Official documentation:** [Update Article](https://developers.forem.com/api/v1#tag/articles/operation/updateArticle)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `article.body_markdown` | body | `string` | no | Article body in Markdown. |
| `article.canonical_url` | body | `string` | no | Optional canonical URL. |
| `article.description` | body | `string` | no | Article description or excerpt. |
| `article.main_image` | body | `string` | no | Optional main image URL. |
| `article.series` | body | `string` | no | Optional series name. |
| `article.tags` | body | `string` | no | Comma-separated article tags. |
| `article.title` | body | `string` | no | Article title. |
| `id` | path | `number` | yes | Numeric article ID. |
| `article.published` | body | `boolean` | no | Whether the article should be published. |
| `article.organization_id` | body | `number` | no | Optional organization ID to publish under. |
