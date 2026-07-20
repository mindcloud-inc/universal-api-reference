# Create Article with HelpDocs

Creates a new article in HelpDocs.

## Endpoint

- **Method:** `POST`
- **Path:** `/article`
- **Base URL:** `https://api.helpdocs.io/v1`
- **Official documentation:** [Create Article](https://apidocs.helpdocs.io/article/8Y2t6NVxeU-creating-an-article)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category_id` | body | `string` | no | Category for the article. |
| `title` | body | `string` | yes | Article title. |
| `body` | body | `string` | no | Article body HTML. |
| `is_published` | body | `boolean` | no | Whether the article is published. |
