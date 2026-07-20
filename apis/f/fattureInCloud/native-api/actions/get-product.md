# Get Product with Fatture in Cloud

Retrieves a product from Fatture in Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/c/:company_id/products/:product_id`
- **Base URL:** `https://api-v2.fattureincloud.it`
- **Official documentation:** [Get Product](https://developers.fattureincloud.it/api-reference/#operation/getProduct)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | path | `number` | yes | The ID of the company. |
| `product_id` | path | `number` | yes | The ID of the product. |
| `fields` | query | `string` | no | List of comma-separated fields. |
| `fieldset` | query | `list` | no | Name of the fieldset. Accepted values: `basic`, `detailed`, `fic_view`. |
