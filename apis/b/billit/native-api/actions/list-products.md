# List Products with Billit

Retrieves Billit products for the authenticated company.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/products`
- **Base URL:** `https://api.sandbox.billit.be`
- **Official documentation:** [List Products](https://docs.billit.be/reference/product_getproducts-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$filter` | query | `string` | no | Optional OData filter for Billit products. |
