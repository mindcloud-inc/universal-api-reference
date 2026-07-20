# Create Sales Invoice Line Item with Microsoft Dynamics 365 BC

## Endpoint

- **Method:** `POST`
- **Path:** `v2.0/companies({{companyId}})/salesInvoices(:invoiceId)/salesInvoiceLines`
- **Base URL:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/api/`
- **API:** REST

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `companyId` | path | `list` | no |
| `unitPrice` | body | `number` | no |
| `invoiceId` | path | `string` | no |
| `quantity` | body | `number` | no |
| `description` | body | `string` | no |
| `lineObjectNumber` | body | `string` | no |
| `lineType` | body | `string` | no |
| `taxCode` | body | `string` | no |
| `discountPercent` | body | `number` | no |
| `discountAmount` | body | `number` | no |
| `taxAreaCode` | body | `string` | no |
