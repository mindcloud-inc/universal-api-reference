# Create Revenue Budget with Acumatica

Create an Income project budget line with account group, cost code, description, original budgeted quantity, UOM, and original budgeted amount. Acumatica may update a line with the same budget keys.

## Endpoint

- **Method:** `PUT`
- **Path:** `/entity/{endpointName}/{endpointVersion}/ProjectBudget`
- **Base URL:** `{uRL}`
- **Official documentation:** [Create Revenue Budget](https://github.com/Acumatica/AcumaticaRESTAPIClientForCSharp/blob/6.0/EndpointDefinitions/Default_24.200.001)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `AccountGroup.value` | body | `string` | no |
| `CostCode.value` | body | `string` | no |
| `Description.value` | body | `string` | no |
| `InventoryID.value` | body | `string` | no |
| `OriginalBudgetedAmount.value` | body | `number` | no |
| `OriginalBudgetedQty.value` | body | `number` | no |
| `ProjectID` | body | `object` | no |
| `ProjectID.value` | body | `string` | no |
| `ProjectTaskID.value` | body | `string` | no |
| `Type.value` | body | `string` | no |
| `UOM.value` | body | `string` | no |
| `ProjectTaskID` | body | `object` | no |
| `InventoryID` | body | `object` | no |
| `AccountGroup` | body | `object` | no |
| `CostCode` | body | `object` | no |
| `Type` | body | `object` | no |
| `Description` | body | `object` | no |
| `OriginalBudgetedQty` | body | `object` | no |
| `UOM` | body | `object` | no |
| `OriginalBudgetedAmount` | body | `object` | no |
