# List Order Addresses with Yampi

Retrieves the addresses for an order in Yampi.

## Endpoint

- **Method:** `GET`
- **Path:** `/:merchantAlias/orders/:orderId/addresses`
- **Base URL:** `https://api.dooki.com.br/v2`
- **Official documentation:** [List Order Addresses](https://docs.yampi.com.br/api-reference/pedidos/enderecos/listar-enderecos-de-um-pedido)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `orderId` | path | `string` | yes |
