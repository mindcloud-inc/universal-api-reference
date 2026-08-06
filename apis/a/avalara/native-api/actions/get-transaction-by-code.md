# Get Transaction By Code with Avalara AvaTax

## Endpoint

- **Method:** `GET`
- **Path:** `companies/:companyCode/transactions/:transactionCode`
- **Base URL:** `{environment}`
- **Official documentation:** [Get Transaction By Code](https://developer.avalara.com/api-reference/avatax/rest/v2/methods/Transactions/GetTransactionByCode/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyCode` | path | `string` | yes | Avalara company code. |
| `transactionCode` | path | `string` | yes | Avalara transaction code. |
| `documentType` | query | `string` | no | Optional document type to disambiguate transactions that share the same code. |
| `$include` | query | `string` | no | Comma-separated related objects to include in the response. |
