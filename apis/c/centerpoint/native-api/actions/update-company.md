# Update Company with Centerpoint

## Endpoint

- **Method:** `PATCH`
- **Path:** `companies/:COMPANY_ID`
- **Base URL:** `https://api.centerpointconnect.io/centerpoint/`
- **Official documentation:** [Update Company](https://api-portal.centerpointconnect.io/portal/catalogue-products/premium-access-product-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/companies/{COMPANY_ID}PATCH)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `COMPANY_ID` | path | `string` | yes | — |
| `name` | body | `string` | no | — |
| `type` | body | `list<string>` | no | Accepted values: `Admin`, `Company`, `Contractor`, `Corporate`, `Residential`, `Vendor`. |
| `salesStatus` | body | `list<string>` | no | Accepted values: `Dead`, `Lead`, `Quoted`, `Sold`. |
| `timeZone` | body | `list<string>` | no | Accepted values: `America/Anchorage`, `America/Chicago`, `America/Denver`, `America/Detroit`, `America/Los_Angeles`, `America/New_York`, `America/Phoenix`, `Pacific/Honolulu`. |
| `custom.customerType` | body | `string` | no | — |
| `options.taxLabelOverride` | body | `string` | no | — |
| `custom.companyPhoneNumber` | body | `string` | no | — |
| `options.billingAddress` | body | `string` | no | — |
| `options.isCreditHold` | body | `boolean` | no | — |
| `options.isTaxExempt` | body | `boolean` | no | — |
| `options.serviceBillingInstructions` | body | `string` | no | — |
| `is_billing` | body | `boolean` | no | — |
| `is_active` | body | `boolean` | no | — |
| `options.serviceWorkInstructions` | body | `string` | no | — |
| `options.laborRates` | body | `string` | no | — |
| `email` | body | `string` | no | — |
| `streetAddress` | body | `string` | no | — |
| `subpremise` | body | `string` | no | — |
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
| `closeRate` | body | `number` | no | — |
| `options` | body | `object` | no | — |
| `custom` | body | `object` | no | — |
