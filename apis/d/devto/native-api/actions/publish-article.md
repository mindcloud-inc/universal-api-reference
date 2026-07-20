# Publish Article with Dev.to

Publishes a new article in Dev.to.

## Endpoint

- **Method:** `POST`
- **Path:** `/articles`
- **Base URL:** `https://dev.to/api`
- **Official documentation:** [Publish Article](https://developers.forem.com/api/v1#tag/articles/operation/createArticle)

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
| `article.published` | body | `boolean` | no | Whether to publish immediately. Defaults to false in DEV. |
| `article.organization_id` | body | `number` | no | Optional organization ID to publish under. |
