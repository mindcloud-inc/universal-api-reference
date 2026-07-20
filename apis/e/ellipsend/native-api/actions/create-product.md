# Create Product with Ellipsend

Creates a new product in Ellipsend.

## Endpoint

- **Method:** `POST`
- **Path:** `/product`
- **Base URL:** `https://api.ellipsend.com/v1`
- **Official documentation:** [Create Product](https://api.ellipsend.com/v1/docs#/Product/post_v1_product)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product` | body | `string` | yes | The product name. |
| `price` | body | `number` | yes | The product price. |
