# Update Reader with KnowledgeOwl

## Endpoint

- **Method:** `PUT`
- **Path:** `/reader/:id.json`
- **Base URL:** `https://app.knowledgeowl.com/api/head`
- **Official documentation:** [Update Reader](https://support.knowledgeowl.com/help/api-endpoint-reference)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `first_name` | body | `string` | no |
| `last_name` | body | `string` | no |
| `status` | body | `string` | no |
