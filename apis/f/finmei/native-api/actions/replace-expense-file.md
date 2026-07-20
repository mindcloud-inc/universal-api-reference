# Replace Expense File with Finmei

## Endpoint

- **Method:** `POST`
- **Path:** `/expenses/:expenseId/file`
- **Base URL:** `https://app.finmei.com/api`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `expenseId` | path | `string` | yes | — |
| `file` | body | `file` | yes | Expense file upload. |
