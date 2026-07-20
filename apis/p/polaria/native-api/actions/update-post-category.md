# Update Post Category with Polaria

Updates an existing post category in Polaria.

## Endpoint

- **Method:** `PUT`
- **Path:** `/faq_categories/[:id]`
- **Base URL:** `https://app.polaria.ai/rest/v2`
- **Official documentation:** [Update Post Category](https://help.polaria.ai/hc/rest-api-post-categories/put-faq_categories-id-update-a-post-category?lang=en)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the post category to update. |
| `title` | body | `string` | no | — |
| `description` | body | `string` | no | — |
| `parent` | body | `number` | no | — |
