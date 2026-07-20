# Create Budget with Sage Intacct

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://api.intacct.com/ia/xml/xmlgw.phtml`
- **Official documentation:** [Create Budget](https://developer.intacct.com/api/general-ledger/budgets/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `budgetId` | body | `string` | yes |
| `description` | body | `string` | yes |
| `defaultBudget` | body | `boolean` | no |
| `periodName` | body | `string` | yes |
| `locationNo` | body | `string` | no |
| `departmentNo` | body | `string` | no |
| `budgetItems[]` | body | `array` | yes |
| `budgetItems[].accountNo` | body | `string` | yes |
| `budgetItems[].amount` | body | `number` | yes |
