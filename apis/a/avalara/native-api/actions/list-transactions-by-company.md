# List Transactions By Company with Avalara AvaTax

## Endpoint

- **Method:** `GET`
- **Path:** `companies/:companyCode/transactions`
- **Base URL:** `{environment}`
- **Official documentation:** [List Transactions By Company](https://developer.avalara.com/api-reference/avatax/rest/v2/methods/Transactions/ListTransactionsByCompany/)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyCode` | path | `string` | yes | Avalara company code. |
| `dataSourceId` | query | `number` | no | Optionally filter transactions to those from a specific data source. |
| `$include` | query | `string` | no | Comma-separated related objects to include in the response. |
