# Get All Products with Jetbuilt

## Endpoint

- **Method:** `GET`
- **Path:** `product_databases/:databaseId/products`
- **Base URL:** `https://app.jetbuilt.com/api/`
- **Official documentation:** [Get All Products](https://api.jetbuilt.com/customers#get-all-products)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `databaseId` | path | `string` | no |
| `min_updated_at` | query | `string` | no |
| `max_updated_at` | query | `string` | no |
| `manufactuer_name` | query | `string` | no |
