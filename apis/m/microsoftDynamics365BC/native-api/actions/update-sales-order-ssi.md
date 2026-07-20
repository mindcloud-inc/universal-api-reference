# Update Sales Order SSI with Microsoft Dynamics 365 BC

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2.0/companies(:id)/salesHeadersSSI(:salesOrderID)`
- **Base URL:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/api/ssi/aapi/`
- **API:** REST (Copy)
- **Official documentation:** [Update Sales Order SSI](https://anotepad.com/notes/ccfg4kec)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | no |
| `salesOrderID` | path | `string` | no |
| `salesforceOrderNo` | body | `string` | no |
| `shipToCode` | body | `string` | no |
| `billAndHoldReturnSSI` | body | `boolean` | no |
| `billToAddress2` | body | `string` | no |
| `billToContactNo` | body | `string` | no |
| `billToCountryRegionCode` | body | `string` | no |
| `billToCounty` | body | `string` | no |
| `billToCustomerNo` | body | `string` | no |
| `billToName` | body | `string` | no |
| `billToPostCode` | body | `string` | no |
| `currencyCode` | body | `string` | no |
| `currencyCode` | body | `string` | no |
| `customerDiscCode` | body | `string` | no |
| `customerPriceGroup` | body | `string` | no |
| `documentDate` | body | `string` | no |
| `documentType` | body | `string` | no |
| `dropShipVendorNoSSI` | body | `string` | no |
| `dueDate` | body | `string` | no |
| `dueDate` | body | `string` | no |
| `earliestShipDateSSI` | body | `string` | no |
| `earliestShipDateSSI` | body | `string` | no |
| `externalDocumentNo` | body | `string` | no |
| `externalDocumentNo` | body | `string` | no |
| `invoiceDiscCode` | body | `string` | no |
| `itemsShipBeforeInvoiceSSI` | body | `boolean` | no |
| `itemsShipBeforeInvoiceSSI` | body | `boolean` | no |
| `latestShipDateSSI` | body | `string` | no |
| `latestShipDateSSI` | body | `string` | no |
| `locationCode` | body | `string` | no |
| `no` | body | `string` | no |
| `orderDate` | body | `string` | no |
| `orderStatusSSI` | body | `string` | no |
| `orderStatusSSI` | body | `string` | no |
| `orderTypeSSI` | body | `string` | no |
| `paymentDiscountPercent` | body | `number` | no |
| `paymentMethodCode` | body | `string` | no |
| `paymentTermsCode` | body | `string` | no |
| `pmtDiscountDate` | body | `string` | no |
| `postingDate` | body | `string` | no |
| `pricesIncludingVAT` | body | `boolean` | no |
| `prmisedDeliveryDate` | body | `string` | no |
| `requestedDeliveryDate` | body | `string` | no |
| `requestedDeliveryDate` | body | `string` | no |
| `salespersonCode` | body | `string` | no |
| `salespersonCode` | body | `string` | no |
| `sellToAddress` | body | `string` | no |
| `sellToAddress2` | body | `string` | no |
| `sellToCity` | body | `string` | no |
| `sellToContact` | body | `string` | no |
| `sellToContactNo` | body | `string` | no |
| `sellToCountryRegionCode` | body | `string` | no |
| `sellToCounty` | body | `string` | no |
| `sellToCustomerName` | body | `string` | no |
| `sellToCustomerName2` | body | `string` | no |
| `sellToCustomerNo` | body | `string` | no |
| `sellToEmail` | body | `string` | no |
| `sellToPhoneNo` | body | `string` | no |
| `sellToPostCode` | body | `string` | no |
| `shipmentDate` | body | `string` | no |
| `shipmentMethodCode` | body | `string` | no |
| `shippingAgentCode` | body | `string` | no |
| `shippingAgentServiceCode` | body | `string` | no |
| `shippingInstructionsSSI` | body | `string` | no |
| `shippingInstructionsSSI` | body | `string` | no |
| `shipToAddress` | body | `string` | no |
| `shipToContact` | body | `string` | no |
| `shipToCountryRegionCode` | body | `string` | no |
| `shipToCounty` | body | `string` | no |
| `shipToName` | body | `string` | no |
| `shipToPhoneNo` | body | `string` | no |
| `shipToPhoneNo` | body | `string` | no |
| `shipToPostCode` | body | `string` | no |
| `shortcutDimension1Code` | body | `string` | no |
| `shortcutDimension2Code` | body | `string` | no |
| `taxAreaCode` | body | `string` | no |
| `taxAreaCode` | body | `string` | no |
| `taxLiable` | body | `boolean` | no |
| `taxLiable` | body | `boolean` | no |
| `vatCountryRegionCode` | body | `string` | no |
| `vatRegistrationNo` | body | `string` | no |
| `vatRegistrationNo` | body | `string` | no |
