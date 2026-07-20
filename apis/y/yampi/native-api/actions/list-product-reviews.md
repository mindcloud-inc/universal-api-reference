# List Product Reviews with Yampi

Retrieves the reviews for a product in Yampi.

## Endpoint

- **Method:** `GET`
- **Path:** `/:merchantAlias/catalog/products/:id/reviews`
- **Base URL:** `https://api.dooki.com.br/v2`
- **Official documentation:** [List Product Reviews](https://docs.yampi.com.br/api-reference/catalogo/produtos/listar-avaliacoes-de-um-produto)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
