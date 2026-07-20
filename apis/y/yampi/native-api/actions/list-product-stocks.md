# List Product Stocks with Yampi

Retrieves SKU stock levels for a product in Yampi.

## Endpoint

- **Method:** `GET`
- **Path:** `/:merchantAlias/catalog/products/:id/stocks`
- **Base URL:** `https://api.dooki.com.br/v2`
- **Official documentation:** [List Product Stocks](https://docs.yampi.com.br/api-reference/catalogo/produtos/listar-estoques-de-todos-os-skus-de-um-produto)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
