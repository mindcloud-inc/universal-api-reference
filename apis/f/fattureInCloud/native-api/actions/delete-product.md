# Delete Product with Fatture in Cloud

Deletes an existing product from Fatture in Cloud.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/c/:company_id/products/:product_id`
- **Base URL:** `https://api-v2.fattureincloud.it`
- **Official documentation:** [Delete Product](https://developers.fattureincloud.it/api-reference/#operation/deleteProduct)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | path | `number` | yes | The ID of the company. |
| `product_id` | path | `number` | yes | The ID of the product. |
