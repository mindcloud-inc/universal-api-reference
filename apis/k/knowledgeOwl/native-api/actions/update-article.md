# Update Article with KnowledgeOwl

## Endpoint

- **Method:** `PUT`
- **Path:** `/article/:id.json`
- **Base URL:** `https://app.knowledgeowl.com/api/head`
- **Official documentation:** [Update Article](https://support.knowledgeowl.com/help/api-endpoint-reference)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `name` | body | `string` | no |
| `current_version.en.title` | body | `string` | no |
| `current_version.en.text` | body | `string` | no |
| `status` | body | `string` | no |
| `visibility` | body | `string` | no |
