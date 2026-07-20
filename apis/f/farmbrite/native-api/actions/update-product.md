# Update product with Farmbrite

Updates an existing product in Farmbrite.

## Endpoint

- **Method:** `PUT`
- **Path:** `/products/:product_id`
- **Base URL:** `https://api.farmbrite.com/v1`
- **Official documentation:** [Update product](https://developers.farmbrite.com/docs/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `product_id` | path | `string` | yes |
| `price` | body | `number` | no |
