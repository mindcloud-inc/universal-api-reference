# Update Project with D-Tools SI

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.d-tools.com/SI/Publish/Projects/Update`
- **Base URL:** `https://api.d-tools.com/SI/`
- **Official documentation:** [Update Project](https://api.d-tools.com/SI/doc/Api/POST-Publish-Projects)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectItemsInfosToDelete[].model` | body | `string` | no |
| `projectItemsInfosToDelete[].quantity` | body | `number` | no |
| `updateProjectItems[].quantity` | body | `number` | no |
| `updateProjectItems[].unitCost` | body | `number` | no |
| `updateProjectItems[].unitPrice` | body | `string` | no |
| `billingAddress.street1` | body | `string` | no |
| `newProjectItems[].id` | body | `string` | no |
| `projectId` | body | `string` | no |
| `projectItemsInfosToDelete[].manufacturer` | body | `string` | no |
| `siteAddress.street1` | body | `string` | no |
| `updateFields[].projectFieldId` | body | `string` | no |
| `updateProjectItems[].componentId` | body | `string` | no |
| `billingAddress.street2` | body | `string` | no |
| `newProjectItems[]` | body | `array<object>` | no |
| `newProjectItems[].typeId` | body | `string` | no |
| `siteAddress.street2` | body | `string` | no |
| `updateFields[].value` | body | `string` | no |
| `billingAddress.city` | body | `string` | no |
| `newProjectItems[].componentId` | body | `string` | no |
| `siteAddress.city` | body | `string` | no |
| `updateProjectItems[]` | body | `array` | no |
| `billingAddress.state` | body | `string` | no |
| `newProjectItems[].manufacturer` | body | `string` | no |
| `projectItemsInfosToDelete[]` | body | `array` | no |
| `siteAddress.state` | body | `string` | no |
| `billingAddress.postalCode` | body | `string` | no |
| `newProjectItems[].model` | body | `string` | no |
| `siteAddress` | body | `object` | no |
| `siteAddress.postalCode` | body | `string` | no |
| `billingAddress` | body | `object` | no |
| `billingAddress.country` | body | `string` | no |
| `newProjectItems[].packageName` | body | `string` | no |
| `siteAddress.country` | body | `string` | no |
| `billingAddress.phone` | body | `string` | no |
| `newProjectItems[].unitCost` | body | `number` | no |
| `siteAddress.phone` | body | `string` | no |
| `updateFields[]` | body | `array` | no |
| `billingAddress.fax` | body | `string` | no |
| `newProjectItems[].unitPrice` | body | `number` | no |
| `siteAddress.fax` | body | `string` | no |
| `newProjectItems[].quantity` | body | `number` | no |
