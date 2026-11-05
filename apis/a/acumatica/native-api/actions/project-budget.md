# Project Budget with Acumatica

Create or update a project budget line, including account group, cost code, type, description, original budgeted quantity, UOM, original budgeted amount, completion percentage, and pending invoice amount.

## Endpoint

- **Method:** `PUT`
- **Path:** `/entity/{endpointName}/{endpointVersion}/ProjectBudget`
- **Base URL:** `{uRL}`
- **Official documentation:** [Project Budget](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/ProjectBudget/Specify-the-Progress-of-a-Project-Task)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `AccountGroup.value` | body | `string` | no |
| `Completed.value` | body | `number` | no |
| `CostCode.value` | body | `string` | no |
| `Description.value` | body | `string` | no |
| `InventoryID.value` | body | `string` | no |
| `OriginalBudgetedAmount.value` | body | `number` | no |
| `OriginalBudgetedQty.value` | body | `number` | no |
| `PendingInvoiceAmount.value` | body | `number` | no |
| `ProjectID` | body | `object` | no |
| `ProjectID.value` | body | `string` | no |
| `ProjectTaskID.value` | body | `string` | no |
| `Type.value` | body | `string` | no |
| `UOM.value` | body | `string` | no |
| `ProjectTaskID` | body | `object` | no |
| `InventoryID` | body | `object` | no |
| `Completed` | body | `object` | no |
| `PendingInvoiceAmount` | body | `object` | no |
| `AccountGroup` | body | `object` | no |
| `CostCode` | body | `object` | no |
| `Type` | body | `object` | no |
| `Description` | body | `object` | no |
| `OriginalBudgetedQty` | body | `object` | no |
| `UOM` | body | `object` | no |
| `OriginalBudgetedAmount` | body | `object` | no |
