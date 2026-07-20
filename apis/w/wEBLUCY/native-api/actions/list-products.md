# List Products with WEBLUCY

Retrieves products from WEBLUCY.

## Endpoint

- **Method:** `GET`
- **Path:** `/products`
- **Base URL:** `https://apps.weblucy.com/api/site`
- **Official documentation:** [List Products](https://websitebuilder.docs.apiary.io/#reference/products/list-and-create/list-all-products)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category_id` | query | `string` | no | Filter products by category ID. |
| `title` | query | `string` | no | Filter products by title. |
