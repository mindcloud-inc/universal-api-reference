# Update Idea with ProdPad

Updates an existing idea in ProdPad.

## Endpoint

- **Method:** `PUT`
- **Path:** `/ideas/:id`
- **Base URL:** `https://api.prodpad.com/v1`
- **Official documentation:** [Update Idea](https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4#/Ideas/PutIdea)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
| `title` | body | `string` | no |
| `description` | body | `string` | no |
| `state` | body | `string` | no |
