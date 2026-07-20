# Create Sales Order Line with Microsoft Dynamics 365 BC

## Endpoint

- **Method:** `POST`
- **Path:** `v2.0/companies(:companyId)/salesOrders(:salesOrderId)/salesOrderLines`
- **Base URL:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/api/`
- **API:** REST
- **Official documentation:** [Create Sales Order Line](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/api-reference/v2.0/api/dynamics_salesorderline_create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `companyId` | path | `list` | no |
| `salesOrderId` | path | `string` | no |
| `description` | body | `string` | no |
| `discountAmount` | body | `number` | no |
| `discountPercent` | body | `number` | no |
| `invoiceQuantity` | body | `number` | no |
| `itemId` | body | `string` | no |
| `itemVariantId` | body | `string` | no |
| `lineObjectNumber` | body | `string` | no |
| `lineType` | body | `string` | no |
| `locationId` | body | `string` | no |
| `quantity` | body | `number` | no |
| `shipmentDate` | body | `string` | no |
| `shipQuantity` | body | `number` | no |
| `taxCode` | body | `string` | no |
| `unitOfMeasureCode` | body | `string` | no |
| `unitOfMeasureId` | body | `string` | no |
| `unitPrice` | body | `number` | no |
