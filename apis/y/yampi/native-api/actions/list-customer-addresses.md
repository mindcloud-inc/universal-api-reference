# List Customer Addresses with Yampi

Retrieves the addresses for a customer in Yampi.

## Endpoint

- **Method:** `GET`
- **Path:** `/:merchantAlias/customers/:customerId/addresses`
- **Base URL:** `https://api.dooki.com.br/v2`
- **Official documentation:** [List Customer Addresses](https://docs.yampi.com.br/api-reference/clientes/enderecos/listar-enderecos-de-um-cliente)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `string` | yes |
