# Get a product choice with ShopWired

Retrieves a product choice from ShopWired by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/products/{product_id}/choices/{id}`
- **Base URL:** `https://api.ecommerceapi.uk/v1`
- **Official documentation:** [Get a product choice](https://shopwired.readme.io/reference/getproductchoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | path | `number` | yes | ID of the product. |
| `id` | path | `number` | yes | ID of the product choice. |
