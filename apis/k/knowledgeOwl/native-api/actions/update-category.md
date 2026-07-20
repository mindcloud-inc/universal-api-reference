# Update Category with KnowledgeOwl

## Endpoint

- **Method:** `PUT`
- **Path:** `/category/:id.json`
- **Base URL:** `https://app.knowledgeowl.com/api/head`
- **Official documentation:** [Update Category](https://support.knowledgeowl.com/help/api-endpoint-reference)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `name.en` | body | `string` | no |
| `visibility` | body | `string` | no |
| `status` | body | `string` | no |
