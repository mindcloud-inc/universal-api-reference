# Create Opportunity with Centerpoint

## Endpoint

- **Method:** `GET`
- **Path:** `opportunities`
- **Base URL:** `https://api.centerpointconnect.io/centerpoint/`
- **Official documentation:** [Create Opportunity](https://api-portal.centerpointconnect.io/portal/catalogue-products/premium-access-product-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/opportunitiesPOST)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `list<string>` | yes | — |
| `options.notifications` | body | `list<string>` | no | — |
| `options.signatureData.isChecked` | body | `boolean` | no | — |
| `name` | body | `string` | no | — |
| `options.contractorNTE` | body | `string` | no | A contractor NTE (Not to Exceed) is a contractual clause and cost-control mechanism that sets a maximum, capped amount a contractor can charge for a project or service. |
| `options.signatureData.name` | body | `string` | no | — |
| `options.nte` | body | `string` | no | Overall opportunity NTE (Not to Exceed) is a contractual clause and cost-control mechanism that sets a maximum, capped amount for the overall opportunity. |
| `options.signatureData.file` | body | `string` | no | — |
| `price` | body | `number` | no | — |
| `opportunityType` | body | `string` | no | — |
| `options.signatureData.date` | body | `string` | no | — |
| `options.truckId` | body | `string` | no | — |
| `options.attachmentId` | body | `string` | no | — |
| `options.signatureData.purchaseOrder` | body | `string` | no | — |
| `workflowType` | body | `string` | no | — |
| `description` | body | `string` | no | — |
| `options.signatureData` | body | `object` | no | — |
| `type` | body | `list<string>` | no | — |
| `propertyID` | body | `string` | no | — |
| `billedCompanyID` | body | `string` | no | — |
| `dueDate` | body | `string` | no | — |
| `forecastedAt` | body | `string` | no | — |
| `projectedCloseDate` | body | `string` | no | — |
| `options` | body | `object` | no | — |
| `custom` | body | `object` | no | — |
