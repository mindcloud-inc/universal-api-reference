# Get a specific product variation with ShopWired

Retrieves a product variation from ShopWired by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/products/{product_id}/variations/{id}`
- **Base URL:** `https://api.ecommerceapi.uk/v1`
- **Official documentation:** [Get a specific product variation](https://shopwired.readme.io/reference/getproductvariationbyid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | path | `number` | yes | The unique identifier of the product. |
| `id` | path | `number` | yes | The unique identifier of the product variation. |
