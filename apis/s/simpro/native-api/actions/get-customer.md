# Get Customer with Simpro

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/:companyId/customers/companies/:customerId`
- **Base URL:** `https://mindcloud.simprosuite.com/api/v1.0`
- **Official documentation:** [Get Customer](https://developer.simprogroup.com/apidoc/?page=e6d0e1c8fc6a4fcf47869df87e04cd88)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `number` | yes | Simpro company ID. Single-company builds usually use 0. |
| `customerId` | path | `number` | yes | Company customer ID. |
| `columns[]` | query | `array<string>` | no | Specific customer fields to return. |
