# Update a Product with Pipedrive

Updates an existing product in Pipedrive.

## Endpoint

- **Method:** `PATCH`
- **Path:** `v2/products/:productId`
- **Base URL:** `{api_domain}/api`
- **Official documentation:** [Update a Product](https://developers.pipedrive.com/docs/api/v1/Products#updateAProduct)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `productId` | path | `number` | yes |
| `name` | body | `string` | no |
| `code` | body | `string` | no |
| `description` | body | `string` | no |
