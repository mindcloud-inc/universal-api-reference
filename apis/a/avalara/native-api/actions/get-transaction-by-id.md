# Get Transaction By Id with Avalara AvaTax

## Endpoint

- **Method:** `GET`
- **Path:** `transactions/:id`
- **Base URL:** `{environment}`
- **Official documentation:** [Get Transaction By Id](https://developer.avalara.com/api-reference/avatax/rest/v2/methods/Transactions/GetTransactionById/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Avalara transaction ID. |
| `$include` | query | `string` | no | Comma-separated related objects to include in the response. |
