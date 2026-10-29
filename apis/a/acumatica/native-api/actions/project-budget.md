# Project Budget with Acumatica

Update a project budget line’s completion percentage and pending invoice amount in Acumatica.

## Endpoint

- **Method:** `PUT`
- **Path:** `/entity/{endpointName}/{endpointVersion}/ProjectBudget`
- **Base URL:** `{uRL}`
- **Official documentation:** [Project Budget](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/ProjectBudget/Specify-the-Progress-of-a-Project-Task)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `Completed.value` | body | `number` | no |
| `InventoryID.value` | body | `string` | no |
| `PendingInvoiceAmount.value` | body | `number` | no |
| `ProjectID` | body | `object` | no |
| `ProjectID.value` | body | `string` | no |
| `ProjectTaskID.value` | body | `string` | no |
| `ProjectTaskID` | body | `object` | no |
| `InventoryID` | body | `object` | no |
| `Completed` | body | `object` | no |
| `PendingInvoiceAmount` | body | `object` | no |
