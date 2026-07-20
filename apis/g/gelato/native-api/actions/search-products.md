# Search Products with Gelato

Finds products in a Gelato catalog by attributes.

## Endpoint

- **Method:** `POST`
- **Path:** `https://product.gelatoapis.com/v3/catalogs/{{catalogUid}}/products:search`
- **Base URL:** `https://order.gelatoapis.com`
- **Official documentation:** [Search Products](https://dashboard.gelato.com/docs/products/product/search/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `catalogUid` | path | `string` | yes |
| `attributeFilters` | body | `object` | no |
