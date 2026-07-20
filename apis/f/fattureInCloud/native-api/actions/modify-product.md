# Modify Product with Fatture in Cloud

Updates an existing product in Fatture in Cloud.

## Endpoint

- **Method:** `PUT`
- **Path:** `/c/:company_id/products/:product_id`
- **Base URL:** `https://api-v2.fattureincloud.it`
- **Official documentation:** [Modify Product](https://developers.fattureincloud.it/api-reference/#operation/modifyProduct)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | path | `number` | yes | The ID of the company. |
| `product_id` | path | `number` | yes | The ID of the product. |
| `data` | body | `object` | yes | The product payload inside the provider data envelope. |
