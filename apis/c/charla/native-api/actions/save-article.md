# Save Article with Charla

Saves an article record in Charla.

## Endpoint

- **Method:** `POST`
- **Path:** `/kb/articles`
- **Base URL:** `https://api.charla.com/v1`
- **Official documentation:** [Save Article](https://charla.com/public-api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `article` | body | `string` | no | HTML or rich-text article content. |
| `categories[].id` | body | `number` | no | Category ID to attach to the article. Add one item per category. |
| `description` | body | `string` | no | Short description of the article. |
| `id` | body | `number` | no | Provide an existing article ID to update that article. |
| `slug` | body | `string` | no | URL slug for the article. |
| `status` | body | `string` | no | Status of the article, for example Draft or Published. |
| `title` | body | `string` | no | Title of the article. |
| `visibility` | body | `string` | no | Visibility of the article, for example Private or Public. |
