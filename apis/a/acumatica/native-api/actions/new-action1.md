# Create Project with Acumatica

## Endpoint

- **Method:** `PUT`
- **Path:** `/entity/:webServiceEndpoint/:endpointVersion/Project`
- **Base URL:** `{uRL}`
- **Official documentation:** [Create Project](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Project/Create-a-Project-from-a-Project-Template?contentId=wJATI0KrOKqQ~ad2W48pHQ)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `billingAndAllocationSettings.billingPeriod.value` | body | `string` | no |
| `billingAndAllocationSettings.billingRule` | body | `object` | no |
| `billingAndAllocationSettings.billingRule.value` | body | `string` | no |
| `customer.value` | body | `string` | no |
| `description.value` | body | `string` | no |
| `ownerId.value` | body | `string` | no |
| `projectId.value` | body | `string` | no |
| `projectTemplateId.value` | body | `string` | no |
| `status.value` | body | `string` | no |
| `webServiceEndpoint` | path | `string` | no |
| `billingAndAllocationSettings.billingPeriod` | body | `object` | no |
| `endpointVersion` | path | `string` | no |
| `projectId` | body | `object` | yes |
| `projectTemplateId` | body | `object` | no |
| `customer` | body | `object` | no |
| `billingAndAllocationSettings` | body | `object` | no |
| `description` | body | `object` | no |
| `ownerId` | body | `object` | no |
| `status` | body | `object` | no |
