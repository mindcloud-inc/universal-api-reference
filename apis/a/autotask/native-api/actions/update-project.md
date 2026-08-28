# Update Project with Autotask

## Endpoint

- **Method:** `PATCH`
- **Path:** `/Projects`
- **Base URL:** `https://webservices14.autotask.net/ATServicesRest/v1.0`
- **Official documentation:** [Update Project](https://www.autotask.net/help/developerhelp/Content/APIs/REST/Entities/ProjectsEntity.htm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | yes | — |
| `projectName` | body | `string` | no | Maximum length: 100. |
| `projectType` | body | `number` | no | Baseline projects are read-only and cannot be updated through the API. |
| `startDateTime` | body | `date` | no | Can be changed only when no phases, tasks, or issues are associated, and must be before the end date. |
| `endDateTime` | body | `date` | no | Must be on or after the latest phase, task, or issue end date. |
| `projectLeadResourceID` | body | `number` | no | — |
| `contractID` | body | `number` | no | — |
| `opportunityID` | body | `number` | no | — |
| `organizationalLevelAssociationID` | body | `number` | no | — |
| `department` | body | `number` | no | — |
| `status` | body | `number` | no | Inactive status inactivates the project; completing a project also completes its associated tasks. |
| `completedDateTime` | body | `date` | no | — |
| `statusDateTime` | body | `date` | no | — |
| `statusDetail` | body | `string` | no | Maximum length: 2000. |
| `description` | body | `string` | no | Maximum length: 2000. |
| `extProjectNumber` | body | `string` | no | Maximum length: 50. |
| `extProjectType` | body | `number` | no | — |
| `purchaseOrderNumber` | body | `string` | no | Maximum length: 50. |
| `estimatedSalesCost` | body | `number` | no | — |
| `laborEstimatedCosts` | body | `number` | no | — |
| `laborEstimatedRevenue` | body | `number` | no | — |
| `originalEstimatedRevenue` | body | `number` | no | — |
| `projectCostsBudget` | body | `number` | no | — |
| `projectCostsRevenue` | body | `number` | no | — |
| `sGDA` | body | `number` | no | — |
| `userDefinedFields[]` | body | `array<object>` | no | Optional project user-defined fields. Multi-select and reference UDFs are not supported. |
| `userDefinedFields[].name` | body | `string` | no | — |
| `userDefinedFields[].value` | body | `string` | no | — |
