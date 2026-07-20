# Create Article with KnowledgeOwl

## Endpoint

- **Method:** `POST`
- **Path:** `/article.json`
- **Base URL:** `https://app.knowledgeowl.com/api/head`
- **Official documentation:** [Create Article](https://support.knowledgeowl.com/help/api-endpoint-reference)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_id` | body | `string` | yes |
| `name` | body | `string` | yes |
| `current_version.en.title` | body | `string` | yes |
| `current_version.en.text` | body | `string` | yes |
| `status` | body | `string` | yes |
| `visibility` | body | `string` | yes |
| `url_hash` | body | `string` | yes |
