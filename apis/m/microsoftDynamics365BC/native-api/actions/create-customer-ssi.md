# Create Customer SSI with Microsoft Dynamics 365 BC

## Endpoint

- **Method:** `POST`
- **Path:** `v2.0/companies(:company_id)/customersSSI`
- **Base URL:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/api/ssi/aapi/`
- **API:** REST (Copy)
- **Official documentation:** [Create Customer SSI](https://anotepad.com/notes/nih23qmd)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `address` | body | `string` | no |
| `company_id` | path | `string` | yes |
| `county` | body | `string` | no |
| `paymentMethodCode` | body | `string` | no |
| `paymentTermsCode` | body | `string` | no |
| `taxAreaCode` | body | `string` | no |
| `salesforceCustomerNo` | body | `string` | no |
| `salespersonCode` | body | `string` | no |
| `no` | body | `string` | no |
| `sICCodeSSI` | body | `string` | no |
| `documentSendingProfile` | body | `string` | no |
| `name` | body | `string` | no |
| `genBusPostingGroup` | body | `string` | no |
| `customerPostingGroup` | body | `string` | no |
| `.addressLine2` | body | `string` | no |
| `.countryRegionCode` | body | `string` | no |
| `balance` | body | `number` | no |
| `balanceLCY` | body | `number` | no |
| `blocked` | body | `string` | no |
| `city` | body | `string` | no |
| `contact` | body | `string` | no |
| `creditLimitLCY` | body | `number` | no |
| `currencyCode` | body | `string` | no |
| `currencyId` | body | `string` | no |
| `email` | body | `string` | no |
| `gln` | body | `string` | no |
| `globalDimension1Code` | body | `string` | no |
| `globalDimension2Code` | body | `string` | no |
| `invoiceAmounts` | body | `number` | no |
| `languageCode` | body | `string` | no |
| `netChange` | body | `number` | no |
| `netChangeLCY` | body | `number` | no |
| `phoneNumber` | body | `string` | no |
| `postCode` | body | `string` | no |
| `priority` | body | `number` | no |
| `responsibilityCenter` | body | `string` | no |
| `salespersonCode` | body | `string` | no |
| `searchName` | body | `string` | no |
| `shipmentMethodCode` | body | `string` | no |
| `shipmentMethodId` | body | `string` | no |
| `stateInscription` | body | `string` | no |
| `taxLiable` | body | `boolean` | no |
| `taxRegistrationNumber` | body | `string` | no |
| `vatBusPostingGroup` | body | `string` | no |
| `vatRegistrationNo` | body | `string` | no |
| `website` | body | `string` | no |
