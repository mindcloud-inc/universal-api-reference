# Create Product with Fatture in Cloud

Creates a new product in Fatture in Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/c/:company_id/products`
- **Base URL:** `https://api-v2.fattureincloud.it`
- **Official documentation:** [Create Product](https://developers.fattureincloud.it/api-reference/#operation/createProduct)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | path | `number` | yes | The ID of the company. |
| `data` | body | `object` | yes | The product payload inside the provider data envelope. |
