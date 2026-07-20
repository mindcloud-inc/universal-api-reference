# List Customer Carts with Yampi

Retrieves abandoned carts for a customer in Yampi.

## Endpoint

- **Method:** `GET`
- **Path:** `/:merchantAlias/customers/:id/carts`
- **Base URL:** `https://api.dooki.com.br/v2`
- **Official documentation:** [List Customer Carts](https://docs.yampi.com.br/api-reference/clientes/listar-carrinhos-abandonados-de-um-cliente)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
