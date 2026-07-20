# Create Objective with ProdPad

Creates a new objective in ProdPad.

## Endpoint

- **Method:** `POST`
- **Path:** `/objectives`
- **Base URL:** `https://api.prodpad.com/v1`
- **Official documentation:** [Create Objective](https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4#/Products/PostObjectives)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | no |
| `state` | body | `string` | no |
| `product.id` | body | `number` | no |
