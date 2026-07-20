# List Product SKUs with Yampi

Retrieves the SKUs for a product in Yampi.

## Endpoint

- **Method:** `GET`
- **Path:** `/:merchantAlias/catalog/products/:id/skus`
- **Base URL:** `https://api.dooki.com.br/v2`
- **Official documentation:** [List Product SKUs](https://docs.yampi.com.br/api-reference/catalogo/produtos/listar-skus-de-um-produto)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
