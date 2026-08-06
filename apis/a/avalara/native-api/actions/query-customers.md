# Query Customers with Avalara AvaTax

## Endpoint

- **Method:** `GET`
- **Path:** `companies/:companyId/customers`
- **Base URL:** `{environment}`
- **Official documentation:** [Query Customers](https://developer.avalara.com/api-reference/avatax/rest/v2/methods/Customers/QueryCustomers/)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `number` | yes | Avalara company ID. |
