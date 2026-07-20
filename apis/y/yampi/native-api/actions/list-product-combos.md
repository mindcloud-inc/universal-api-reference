# List Product Combos with Yampi

Retrieves the combos for a product in Yampi.

## Endpoint

- **Method:** `GET`
- **Path:** `/:merchantAlias/catalog/products/:id/combos`
- **Base URL:** `https://api.dooki.com.br/v2`
- **Official documentation:** [List Product Combos](https://docs.yampi.com.br/api-reference/catalogo/produtos/listar-combos-de-um-produto)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
