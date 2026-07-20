# Create Customer with Simpro

## Endpoint

- **Method:** `POST`
- **Path:** `/companies/:companyId/customers/companies/`
- **Base URL:** `https://mindcloud.simprosuite.com/api/v1.0`
- **Official documentation:** [Create Customer](https://developer.simprogroup.com/apidoc/?page=e6d0e1c8fc6a4fcf47869df87e04cd88)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `number` | yes | Simpro company ID. Single-company builds usually use 0. |
| `CompanyName` | body | `string` | yes | Company customer name. |
| `Email` | body | `string` | no | Customer email address. |
| `Phone` | body | `string` | no | Customer telephone number. |
| `createSite` | query | `boolean` | no | Whether Simpro should create a site with the customer. |
