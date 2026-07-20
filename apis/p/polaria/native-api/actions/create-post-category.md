# Create Post Category with Polaria

Creates a new post category in Polaria.

## Endpoint

- **Method:** `POST`
- **Path:** `/faq_categories`
- **Base URL:** `https://app.polaria.ai/rest/v2`
- **Official documentation:** [Create Post Category](https://help.polaria.ai/hc/rest-api-post-categories/post-faq_categories-create-a-post-category?lang=en)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `title` | body | `string` | yes |
| `description` | body | `string` | no |
| `parent` | body | `number` | no |
