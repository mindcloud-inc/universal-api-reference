# List Products with Keysender

Retrieves products from Keysender.

## Endpoint

- **Method:** `GET`
- **Path:** `/catalog/products`
- **Base URL:** `https://panel.keysender.co.uk/api/v1.0`
- **Official documentation:** [List Products](https://panel.keysender.co.uk/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Catalog page number. Keysender uses 1-based pages. |
| `items_per_page` | query | `number` | no | Number of products to return per page. |
| `additional_information` | query | `boolean` | no | Include expanded product information when true. |
