# Update Article with HelpDocs

Updates an existing article in HelpDocs.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/article/:article_id`
- **Base URL:** `https://api.helpdocs.io/v1`
- **Official documentation:** [Update Article](https://apidocs.helpdocs.io/category/Z83io6YtSs-articles)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `article_id` | path | `string` | yes | Article ID to update. |
| `body` | body | `string` | no | Updated article body HTML. |
| `title` | body | `string` | no | Updated article title. |
| `is_published` | body | `boolean` | no | Whether the article is published. |
