# Create Property with Centerpoint

## Endpoint

- **Method:** `POST`
- **Path:** `properties`
- **Base URL:** `https://api.centerpointconnect.io/centerpoint/`
- **Official documentation:** [Create Property](https://api-portal.centerpointconnect.io/portal/catalogue-products/premium-access-product-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/propertiesPOST)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `custom.roofSize` | body | `string` | no | — |
| `name` | body | `string` | yes | — |
| `options.billingAddress` | body | `string` | no | — |
| `options.isCreditHold` | body | `boolean` | no | — |
| `options.isTaxExempt` | body | `boolean` | no | — |
| `accountId` | body | `number` | no | — |
| `options.serviceBillingInstructions` | body | `string` | no | — |
| `companyId` | body | `list<number>` | no | — |
| `options.serviceWorkInstructions` | body | `string` | no | — |
| `options.interactivePropertyUrl` | body | `string` | no | — |
| `primaryContractorID` | body | `number` | no | — |
| `options.taxCodeIDs[]` | body | `array<number>` | no | — |
| `primaryBuildingID` | body | `number` | no | Maximum length: 0. |
| `externalID` | body | `string` | no | Maximum length: 100. |
| `importID` | body | `string` | no | Maximum length: 255. |
| `managerID` | body | `number` | no | — |
| `locationID` | body | `number` | no | — |
| `options` | body | `object` | no | — |
| `custom` | body | `object` | no | — |
