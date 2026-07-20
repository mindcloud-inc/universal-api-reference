# Create Article with Document360

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/Articles`
- **Base URL:** `https://apihub.document360.io`
- **Official documentation:** [Create Article](https://apidocs.document360.com/apidocs/add-an-article)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | The title of the article |
| `content` | body | `string` | no | The article content |
| `category_id` | body | `string` | no | The category where the article will be created |
| `project_version_id` | body | `string` | yes | The project version where the article will be created |
| `user_id` | body | `string` | yes | The team account that will be marked as contributor |
| `order` | body | `number` | no | The position inside the category |
| `content_type` | body | `number` | no | The editor type |
| `slug` | body | `string` | no | Optional custom slug |
