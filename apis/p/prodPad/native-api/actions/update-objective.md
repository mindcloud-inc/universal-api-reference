# Update Objective with ProdPad

Updates an existing objective in ProdPad.

## Endpoint

- **Method:** `PUT`
- **Path:** `/objectives/:id`
- **Base URL:** `https://api.prodpad.com/v1`
- **Official documentation:** [Update Objective](https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4#/Products/PutObjective)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `name` | body | `string` | no |
| `state` | body | `string` | no |
| `product.id` | body | `number` | no |
