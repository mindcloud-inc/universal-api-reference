# Update Property with Centerpoint

## Endpoint

- **Method:** `PATCH`
- **Path:** `properties/:PROPERTY_ID`
- **Base URL:** `https://api.centerpointconnect.io/centerpoint/`
- **Official documentation:** [Update Property](https://api-portal.centerpointconnect.io/portal/catalogue-products/premium-access-product-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/properties/%7BPROPERTY_ID%7DPATCH)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PROPERTY_ID` | path | `string` | yes | Centerpoint property id to update. Use the property id from List Properties. |
| `name` | body | `string` | no | Centerpoint property name. |
| `visible` | body | `boolean` | no | Whether the Centerpoint property is visible. |
| `timeZone` | body | `string` | no | Property timezone, for example America/Chicago. |
| `accountId` | body | `number` | no | Centerpoint account id for the property. |
| `companyId` | body | `list<number>` | no | Centerpoint company id for the property. |
| `primaryContractorID` | body | `number` | no | Centerpoint primary contractor id for the property. |
| `externalID` | body | `string` | no | Existing Centerpoint property external id. Do not map CompanyCam here unless this identifier is explicitly owned by the CompanyCam sync. Maximum length: 100. |
| `primaryBuildingID` | body | `number` | no | Centerpoint primary building id for the property. |
| `importID` | body | `string` | no | Centerpoint import id for the property. Maximum length: 255. |
| `managerID` | body | `number` | no | Centerpoint manager id for the property. |
| `locationID` | body | `number` | no | Centerpoint location id for the property. |
| `options` | body | `object` | no | Optional Centerpoint property options object. |
| `options.billingAddress` | body | `string` | no | Property billing address in Centerpoint options. |
| `options.isCreditHold` | body | `boolean` | no | Whether the property is on credit hold. |
| `options.isTaxExempt` | body | `boolean` | no | Whether the property is tax exempt. |
| `options.serviceBillingInstructions` | body | `string` | no | Service billing instructions in Centerpoint options. |
| `options.serviceWorkInstructions` | body | `string` | no | Service work instructions in Centerpoint options. |
| `options.interactivePropertyUrl` | body | `string` | no | Interactive property URL in Centerpoint options. |
| `options.taxCodeIDs[]` | body | `array<number>` | no | Centerpoint tax code ids for the property. |
| `custom` | body | `object` | no | Centerpoint custom fields object. |
| `custom.CompanyCam Project ID` | body | `string` | no | CompanyCam project id linked to this Centerpoint property. |
| `custom.CompanyCam Project URL` | body | `string` | no | CompanyCam project URL linked to this Centerpoint property. |
| `custom.roofSize` | body | `string` | no | Property roof size custom field. |
