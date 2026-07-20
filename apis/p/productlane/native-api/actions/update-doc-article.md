# Update Doc Article with Productlane

Updates a help center article in Productlane.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/docs/articles/{id}`
- **Base URL:** `https://productlane.com/api/v1`
- **Official documentation:** [Update Doc Article](https://productlane.mintlify.dev/docs/api/docs/update-doc-article)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Doc article ID. |
| `title` | body | `string` | no | Updated article title. |
| `content` | body | `string` | no | Updated markdown content. |
| `summary` | body | `string` | no | Updated article summary. |
| `published` | body | `boolean` | no | Whether the article is published. |
| `archived` | body | `boolean` | no | Whether the article is archived. |
| `showOnHomePage` | body | `boolean` | no | Whether to feature the article on the home page. |
