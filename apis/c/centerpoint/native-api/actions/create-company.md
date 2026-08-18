# Create Company with Centerpoint

## Endpoint

- **Method:** `POST`
- **Path:** `companies`
- **Base URL:** `https://api.centerpointconnect.io/centerpoint/`
- **Official documentation:** [Create Company](https://api-portal.centerpointconnect.io/portal/catalogue-products/premium-access-product-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/companiesPOST)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `custom.customerType` | body | `string` | no | — |
| `name` | body | `string` | yes | — |
| `options.taxLabelOverride` | body | `string` | no | — |
| `custom.companyphonenumber` | body | `string` | no | — |
| `options.billingAddress` | body | `string` | no | — |
| `type` | body | `list<string>` | yes | — |
| `options.isCreditHold` | body | `boolean` | no | — |
| `salesStatus` | body | `list<string>` | yes | — |
| `options.isTaxExempt` | body | `boolean` | no | — |
| `timezone` | body | `list<string>` | yes | — |
| `is_billing` | body | `boolean` | no | — |
| `options.serviceBillingInstructions` | body | `string` | no | — |
| `is_active` | body | `boolean` | no | — |
| `options.serviceWorkInstructions` | body | `string` | no | — |
| `email` | body | `string` | no | Maximum length: 0. |
| `options.laborRates` | body | `string` | no | — |
| `streetAddress` | body | `string` | no | — |
| `subpremise` | body | `string` | no | Maximum length: 100. |
| `locality` | body | `string` | no | — |
| `county` | body | `string` | no | — |
| `region` | body | `string` | no | — |
| `postalCode` | body | `string` | no | — |
| `country` | body | `string` | no | — |
| `latitude` | body | `number` | no | — |
| `longitude` | body | `number` | no | — |
| `placeId` | body | `string` | no | — |
| `externalId` | body | `string` | no | — |
| `importId` | body | `string` | no | — |
| `managerId` | body | `string` | no | — |
| `website` | body | `string` | no | — |
| `imageID` | body | `string` | no | — |
| `closeRate` | body | `number` | no | Percentage number between 0 and 1 |
| `options` | body | `object` | no | — |
| `custom` | body | `object` | no | — |
