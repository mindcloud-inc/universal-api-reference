# Publish Projects with D-Tools SI

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.d-tools.com/SI/Publish/Projects`
- **Base URL:** `https://api.d-tools.com/SI/`
- **Official documentation:** [Publish Projects](https://api.d-tools.com/SI/doc/Api/POST-Publish-Projects)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `billingAddress.street1` | body | `string` | no |
| `contacts[].name` | body | `string<object>` | no |
| `items[].id` | body | `string` | no |
| `locations[].id` | body | `string<object>` | no |
| `siteAddress.street1` | body | `string` | no |
| `templateName` | body | `string` | no |
| `billingAddress.street2` | body | `string` | no |
| `contacts[].email` | body | `string<object>` | no |
| `items[]` | body | `array<object>` | no |
| `items[].typeId` | body | `string` | no |
| `locations[].name` | body | `string<object>` | no |
| `siteAddress.street2` | body | `string` | no |
| `billingAddress.city` | body | `string` | no |
| `contacts[].phone` | body | `string<object>` | no |
| `items[].componentId` | body | `string` | no |
| `locations[].description` | body | `string<object>` | no |
| `packages[]` | body | `array` | no |
| `siteAddress.city` | body | `string` | no |
| `billingAddress.state` | body | `string` | no |
| `items[].manufacturer` | body | `string` | no |
| `publishedOn` | body | `date` | no |
| `siteAddress.state` | body | `string` | no |
| `billingAddress.postalCode` | body | `string` | no |
| `id` | body | `string` | no |
| `items[].model` | body | `string` | no |
| `siteAddress.postalCode` | body | `string` | no |
| `billingAddress.country` | body | `string` | no |
| `integrationProjectId` | body | `string` | no |
| `items[].packageName` | body | `string` | no |
| `siteAddress.country` | body | `string` | no |
| `billingAddress.phone` | body | `string` | no |
| `client` | body | `string` | yes |
| `items[].unitCost` | body | `number` | no |
| `siteAddress.phone` | body | `string` | no |
| `billingAddress.fax` | body | `string` | no |
| `clientId` | body | `string` | no |
| `items[].unitPrice` | body | `number` | no |
| `siteAddress.fax` | body | `string` | no |
| `integrationClientId` | body | `string` | no |
| `items[].quantity` | body | `number` | no |
| `clientNumber` | body | `string` | no |
| `name` | body | `string` | yes |
| `number` | body | `string` | no |
| `quantityBased` | body | `boolean` | no |
| `progress` | body | `string` | no |
| `assignedTo` | body | `string` | no |
| `salesRep` | body | `string` | no |
| `projectManager` | body | `string` | no |
| `designer` | body | `string` | no |
| `revision` | body | `number` | no |
| `currencyCode` | body | `string` | no |
| `currencyRate` | body | `number` | no |
| `cost` | body | `number` | no |
| `priceWithoutTax` | body | `number` | no |
| `margin` | body | `number` | no |
| `markup` | body | `number` | no |
| `tax` | body | `number` | no |
| `price` | body | `number` | no |
| `hours` | body | `number` | no |
| `budget` | body | `number` | no |
| `productPriceType` | body | `string` | no |
| `clientPONumber` | body | `string` | no |
| `startDate` | body | `date` | no |
| `endDate` | body | `date` | no |
| `estimatedCloseDate` | body | `date` | no |
| `closeDate` | body | `date` | no |
| `accountingEstimateNumbers` | body | `string` | no |
| `scopeOfWork` | body | `string` | no |
| `notes` | body | `string` | no |
| `siteAddress` | body | `object` | no |
| `billingAddress` | body | `object` | no |
| `isItemLevelTax` | body | `boolean` | no |
| `productTaxId` | body | `string` | no |
| `laborTaxId` | body | `string` | no |
| `approved` | body | `boolean` | no |
| `contacts[]` | body | `array<object>` | no |
| `locations[]` | body | `array<object>` | no |
