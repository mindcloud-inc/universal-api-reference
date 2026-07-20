# Delete Product or All Products with Starshipit

## Endpoint

- **Method:** `DELETE`
- **Path:** `/products/delete`
- **Base URL:** `https://api.starshipit.com/api`
- **Official documentation:** [Delete Product or All Products](https://api-docs.starshipit.com/#5edb43f1-432b-4d1a-bb31-e05db0c879e3)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `product_ids[]` | body | `array<number>` | no |
| `all_products` | body | `boolean` | no |
