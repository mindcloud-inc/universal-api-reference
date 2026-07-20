# Upsert Products with Tidio

Upserts products in the Tidio product catalog.

## Endpoint

- **Method:** `PUT`
- **Path:** `/products/batch`
- **Base URL:** `https://api.tidio.com`
- **Official documentation:** [Upsert Products](https://developers.tidio.com/reference/put_products-batch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `products` | body | `list<object>` | yes | List of products to upsert. Maximum 100 products per request. |
| `products[].id` | body | `number` | yes | Unique identifier for the product. |
| `products[].url` | body | `string` | yes | Direct URL of the product. |
| `products[].image_url` | body | `string` | no | Default image URL of the product. |
| `products[].title` | body | `string` | yes | Title of the product. |
| `products[].description` | body | `string` | yes | Product description. |
| `products[].default_currency` | body | `string` | yes | Default currency code for the product. |
| `products[].vendor` | body | `string` | no | Brand or supplier of the product. |
| `products[].product_type` | body | `string` | no | Category or type of product. |
| `products[].status` | body | `string` | yes | Determines if the product should be recommended by Lyro. |
| `products[].price` | body | `number` | yes | Product price. |
| `products[].sku` | body | `string` | no | Stock Keeping Unit identifier. |
| `products[].barcode` | body | `string` | no | Barcode of the product. |
| `products[].features` | body | `object` | yes | Key-value dictionary for product features and configurable options. |
| `products[].updated_at` | body | `date` | yes | Last update timestamp in ISO 8601 format. |
