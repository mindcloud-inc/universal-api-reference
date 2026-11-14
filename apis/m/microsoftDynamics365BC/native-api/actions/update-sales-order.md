# Update Sales Order with Microsoft Dynamics 365 BC

## Endpoint

- **Method:** `PATCH`
- **Path:** `v2.0/companies(:companyId)/salesOrders(:salesOrderId)`
- **Base URL:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/api/`
- **API:** REST
- **Official documentation:** [Update Sales Order](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/api-reference/v2.0/api/dynamics_salesorder_update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `billToCustomerId` | body | `string` | no | The ID (GUID) of the bill-to customer. |
| `billToCustomerNumber` | body | `string` | no | The number of the bill-to customer. |
| `companyId` | path | `list<string>` | yes | The Business Central company that holds the sales order. |
| `currencyCode` | body | `string` | no | The currency code for the sales order. |
| `currencyId` | body | `string` | no | The ID (GUID) of the currency the sales order uses. |
| `customerId` | body | `string` | no | The ID (GUID) of the sell-to customer. |
| `customerNumber` | body | `string` | no | The number of the sell-to customer. |
| `discountAmount` | body | `number` | no | The sales order discount amount. |
| `email` | body | `string` | no | The sales order's email address. |
| `externalDocumentNumber` | body | `string` | no | An external document number for the sales order, such as the customer's PO number. |
| `orderDate` | body | `string` | no | The order date, in YYYY-MM-DD format. |
| `partialShipping` | body | `boolean` | no | Whether partial shipping of items is preferred. |
| `paymentTermsId` | body | `string` | no | The ID (GUID) of the payment terms the sales order uses. |
| `phoneNumber` | body | `string` | no | The sales order's telephone number. |
| `postingDate` | body | `string` | no | The date the sales order is posted, in YYYY-MM-DD format. |
| `requestedDeliveryDate` | body | `string` | no | The requested delivery date, in YYYY-MM-DD format. |
| `salesOrderId` | path | `string` | yes | The sales order's system ID (GUID), not the order number. |
| `salesperson` | body | `string` | no | The salesperson code for the sales order. |
| `sellToAddressLine1` | body | `string` | no | Sell-to address line 1. |
| `sellToAddressLine2` | body | `string` | no | Sell-to address line 2. |
| `sellToCity` | body | `string` | no | Sell-to city. |
| `sellToCountry` | body | `string` | no | Sell-to country/region code. |
| `sellToPostCode` | body | `string` | no | Sell-to post code. |
| `sellToState` | body | `string` | no | Sell-to state. |
| `shipmentMethodId` | body | `string` | no | The ID (GUID) of the shipment method the sales order uses. |
| `shipToAddressLine1` | body | `string` | no | Ship-to address line 1. |
| `shipToAddressLine2` | body | `string` | no | Ship-to address line 2. |
| `shipToCity` | body | `string` | no | Ship-to city. |
| `shipToContact` | body | `string` | no | The ship-to contact. |
| `shipToCountry` | body | `string` | no | Ship-to country/region code. |
| `shipToName` | body | `string` | no | The ship-to name. |
| `shipToPostCode` | body | `string` | no | Ship-to post code. |
| `shipToState` | body | `string` | no | Ship-to state. |
| `shortcutDimension1Code` | body | `string` | no | The code for shortcut dimension 1. |
| `shortcutDimension2Code` | body | `string` | no | The code for shortcut dimension 2. |
