# Delete Sales Invoice Line Item with Microsoft Dynamics 365 BC

## Endpoint

- **Method:** `DELETE`
- **Path:** `v2.0/companies(:companyId)/salesInvoices(:salesInvoiceId)/salesInvoiceLines(:lineItemId)`
- **Base URL:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/api/`
- **API:** REST
- **Official documentation:** [Delete Sales Invoice Line Item](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/api-reference/v2.0/api/dynamics_customer_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `list<string>` | no | The Id of the company. This Id can be find on the "Get Companies" Action |
| `salesInvoiceId` | path | `string` | no | — |
| `lineItemId` | path | `string` | no | — |
