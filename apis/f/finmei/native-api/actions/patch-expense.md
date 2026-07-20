# Patch Expense with Finmei

## Endpoint

- **Method:** `PATCH`
- **Path:** `/expenses/:expenseId`
- **Base URL:** `https://app.finmei.com/api`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `currency` | body | `string` | no | Expense currency code. |
| `date` | body | `date` | no | Expense date. |
| `expenseId` | path | `string` | yes | — |
| `seller` | body | `string` | no | Expense seller name. |
| `total` | body | `number` | no | Expense total amount. |
