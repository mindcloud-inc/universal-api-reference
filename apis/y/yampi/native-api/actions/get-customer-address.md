# Get Customer Address with Yampi

Retrieves the specified customer address from Yampi.

## Endpoint

- **Method:** `GET`
- **Path:** `/:merchantAlias/customers/:customerId/addresses/:id`
- **Base URL:** `https://api.dooki.com.br/v2`
- **Official documentation:** [Get Customer Address](https://docs.yampi.com.br/api-reference/clientes/enderecos/visualizar-endereco-do-cliente)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `string` | yes |
| `id` | path | `string` | yes |
