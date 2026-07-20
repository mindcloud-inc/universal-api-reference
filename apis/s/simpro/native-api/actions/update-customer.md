# Update Customer with Simpro

## Endpoint

- **Method:** `PATCH`
- **Path:** `/companies/:companyId/customers/companies/:customerId`
- **Base URL:** `https://mindcloud.simprosuite.com/api/v1.0`
- **Official documentation:** [Update Customer](https://developer.simprogroup.com/apidoc/?page=e6d0e1c8fc6a4fcf47869df87e04cd88)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `number` | yes | Simpro company ID. Single-company builds usually use 0. |
| `customerId` | path | `number` | yes | Company customer ID. |
| `CompanyName` | body | `string` | no | Updated company customer name. |
| `Email` | body | `string` | no | Updated customer email. |
| `Phone` | body | `string` | no | Updated customer telephone number. |
