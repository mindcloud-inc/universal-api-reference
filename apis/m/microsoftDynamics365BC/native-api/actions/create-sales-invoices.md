# Create Sales Invoices with Microsoft Dynamics 365 BC

## Endpoint

- **Method:** `POST`
- **Path:** `v2.0/companies({{companyId}})/salesInvoices`
- **Base URL:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/api/`
- **API:** REST

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `companyId` | path | `list` | no |
| `externalDocumentNumber` | body | `string` | no |
| `customerNumber` | body | `string` | no |
| `invoiceDate` | body | `string` | no |
| `taxAreaCode` | body | `string` | no |
| `shortcutDimension1Code` | body | `string` | no |
| `shortcutDimension2Code` | body | `string` | no |
