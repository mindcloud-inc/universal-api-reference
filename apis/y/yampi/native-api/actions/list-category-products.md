# List Category Products with Yampi

Retrieves products assigned to a category in Yampi.

## Endpoint

- **Method:** `GET`
- **Path:** `/:merchantAlias/catalog/categories/:id/products`
- **Base URL:** `https://api.dooki.com.br/v2`
- **Official documentation:** [List Category Products](https://docs.yampi.com.br/api-reference/catalogo/categorias/listar-produtos-associados-a-uma-categoria)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
