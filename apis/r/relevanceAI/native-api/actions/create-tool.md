# Create Tool with Relevance AI

## Endpoint

- **Method:** `POST`
- **Path:** `/studios/bulk_update`
- **Base URL:** `https://api-{region}.stack.tryrelevance.com/latest`
- **Official documentation:** [Create Tool](https://sdk.relevanceai.com/concepts/10_1/tools)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `description` | body | `string` | yes |
| `public` | body | `boolean` | no |
| `title` | body | `string` | yes |
| `toolId` | body | `string` | yes |
