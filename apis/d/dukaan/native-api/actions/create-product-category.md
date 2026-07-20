# Create Product Category with Dukaan

Creates a new product category in Dukaan.

## Endpoint

- **Method:** `POST`
- **Path:** `api/product/seller/product-category/`
- **Base URL:** `https://api.mydukaan.io`
- **Official documentation:** [Create Product Category](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Category name. |
| `store` | body | `string` | yes | Store UUID or ID for the category. |
| `show_to` | body | `number` | no | Dukaan visibility value for the category. |
