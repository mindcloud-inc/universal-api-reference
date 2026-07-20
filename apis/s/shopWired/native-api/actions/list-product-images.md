# List product images with ShopWired

Retrieves images for a product from ShopWired.

## Endpoint

- **Method:** `GET`
- **Path:** `/products/{product_id}/images`
- **Base URL:** `https://api.ecommerceapi.uk/v1`
- **Official documentation:** [List product images](https://shopwired.readme.io/reference/listproductimages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | path | `number` | yes | ID of the product which the images are assigned to. |
