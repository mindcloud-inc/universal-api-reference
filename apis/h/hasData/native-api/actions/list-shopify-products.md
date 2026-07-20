# List Shopify Products with HasData

Retrieves Shopify products from HasData.

## Endpoint

- **Method:** `GET`
- **Path:** `/scrape/shopify/products`
- **Base URL:** `https://api.hasdata.com`
- **Official documentation:** [List Shopify Products](https://docs.hasdata.com/apis/shopify/products)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection` | query | `string` | no | Collection handle to filter products. |
| `limit` | query | `number` | no | Maximum number of products to retrieve. |
| `page` | query | `number` | no | Page number of product results. |
| `url` | query | `string` | yes | Shopify store URL. |
