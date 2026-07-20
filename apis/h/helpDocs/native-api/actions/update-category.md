# Update Category with HelpDocs

Updates an existing category in HelpDocs.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/category/:category_id`
- **Base URL:** `https://api.helpdocs.io/v1`
- **Official documentation:** [Update Category](https://apidocs.helpdocs.io/article/9f9mMkb0od-updating-a-category)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category_id` | path | `string` | yes | Category ID to update. |
| `description` | body | `string` | no | Updated category description. |
| `title` | body | `string` | no | Updated category title. |
