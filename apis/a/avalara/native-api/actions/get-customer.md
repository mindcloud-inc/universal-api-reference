# Get Customer with Avalara AvaTax

## Endpoint

- **Method:** `GET`
- **Path:** `companies/:companyId/customers/:customerCode`
- **Base URL:** `{environment}`
- **Official documentation:** [Get Customer](https://developer.avalara.com/api-reference/avatax/rest/v2/methods/Customers/GetCustomer/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `number` | yes | Avalara company ID. |
| `customerCode` | path | `string` | yes | Avalara customer code. |
