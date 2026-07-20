# List Product Promotions with Yampi

Retrieves the promotions for a product in Yampi.

## Endpoint

- **Method:** `GET`
- **Path:** `/:merchantAlias/catalog/products/:id/promotions`
- **Base URL:** `https://api.dooki.com.br/v2`
- **Official documentation:** [List Product Promotions](https://docs.yampi.com.br/api-reference/catalogo/produtos/listar-promocoes-que-um-produto-pertence)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
