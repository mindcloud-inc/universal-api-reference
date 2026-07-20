# Delete Product Sample with Tiliter

Deletes a product sample from the Tiliter Recognition API.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/products/:product_id/samples/:sample_id`
- **Base URL:** `https://recognition.services.tiliter.com/v1/15`
- **Official documentation:** [Delete Product Sample](https://developer.tiliter.com/reference/delete_product_sample)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `product_id` | path | `string` | yes |
| `sample_id` | path | `string` | yes |
