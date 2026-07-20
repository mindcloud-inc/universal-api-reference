# Update Product with Kiwili

Updates an existing product in Kiwili.

## Endpoint

- **Method:** `PUT`
- **Path:** `/product/:product_id`
- **Base URL:** `https://mindcloud.kiwili.com/api`
- **Official documentation:** [Update Product](https://api.kiwili.com/api/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Active` | body | `boolean` | no | Whether the product is active. |
| `Name` | body | `string` | no | The updated product name. |
| `Price` | body | `number` | no | The updated product price. |
| `product_id` | path | `number` | yes | The Kiwili product ID to update. |
