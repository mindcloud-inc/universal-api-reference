# Create Sales Order with Microsoft Dynamics 365 BC

## Endpoint

- **Method:** `POST`
- **Path:** `companies(:id)/salesOrders`
- **Base URL:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/api/`
- **API:** REST
- **Official documentation:** [Create Sales Order](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/api-reference/v2.0/api/dynamics_salesorder_create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | no |
| `orderDate` | body | `string` | no |
| `customerId` | body | `string` | no |
| `externalDocumentNumber` | body | `string` | no |
| `billToAddressLine1` | body | `string` | no |
| `currencyCode` | body | `string` | no |
| `customerName` | body | `string` | no |
| `customerNumber` | body | `string` | no |
| `discountAmount` | body | `number` | no |
| `discountAppliedBeforeTax` | body | `boolean` | no |
| `documentLines[]` | body | `array` | no |
| `email` | body | `string` | no |
| `fullyShipped` | body | `boolean` | no |
| `lastModifiedDateTime` | body | `string` | no |
| `partialShipping` | body | `boolean` | no |
| `paymentTermsId` | body | `string` | no |
| `phoneNumber` | body | `string` | no |
| `postingDate` | body | `string` | no |
| `pricesIncludeTax` | body | `boolean` | no |
| `requestedDeliveryDate` | body | `string` | no |
| `salesperson` | body | `string` | no |
| `sellToAddressLine1` | body | `string` | no |
| `shipmentMethodId` | body | `string` | no |
| `shipToName` | body | `string` | no |
| `shortcutDimension1Code` | body | `string` | no |
| `shortcutDimension2Code` | body | `string` | no |
| `status` | body | `string` | no |
| `totalAmountExcludingTax` | body | `number` | no |
| `totalAmountIncludingTax` | body | `number` | no |
| `totalTaxAmount` | body | `number` | no |
