# Create Category with Document360

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/Categories`
- **Base URL:** `https://apihub.document360.io`
- **Official documentation:** [Create Category](https://apidocs.document360.com/apidocs/add-a-category)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the category |
| `project_version_id` | body | `string` | yes | Project version where the category will be created |
| `order` | body | `number` | no | The position inside the parent category |
| `parent_category_id` | body | `string` | no | Parent category for nesting |
| `content` | body | `string` | no | Category content for page or index categories |
| `category_type` | body | `number` | yes | 0 Folder, 1 Page, 2 Index |
| `user_id` | body | `string` | yes | Team account ID creating the category |
| `content_type` | body | `number` | no | 0 Markdown, 1 WYSIWYG, 2 Advanced WYSIWYG |
| `slug` | body | `string` | no | Optional URL-friendly slug |
