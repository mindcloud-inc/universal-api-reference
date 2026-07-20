# List Order Items with Yampi

Retrieves the items for an order in Yampi.

## Endpoint

- **Method:** `GET`
- **Path:** `/:merchantAlias/orders/:id/items`
- **Base URL:** `https://api.dooki.com.br/v2`
- **Official documentation:** [List Order Items](https://docs.yampi.com.br/api-reference/pedidos/pedido/listar-produtos-de-um-pedido)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
