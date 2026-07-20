# List Order Tracking with Yampi

Retrieves tracking details for an order in Yampi.

## Endpoint

- **Method:** `GET`
- **Path:** `/:merchantAlias/orders/:id/tracking`
- **Base URL:** `https://api.dooki.com.br/v2`
- **Official documentation:** [List Order Tracking](https://docs.yampi.com.br/api-reference/pedidos/rastreamento/rastrear-pedido)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
