# Get a product option with ShopWired

Retrieves a product option from ShopWired by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/products/{product_id}/options/{id}`
- **Base URL:** `https://api.ecommerceapi.uk/v1`
- **Official documentation:** [Get a product option](https://shopwired.readme.io/reference/getproductoptionbyid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | path | `number` | yes | ID of the product which the option is assigned to. |
| `id` | path | `number` | yes | ID of the product option. |
