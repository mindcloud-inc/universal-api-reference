# Create Expense with Moxie

Creates a new expense in Moxie.

## Endpoint

- **Method:** `POST`
- **Path:** `/action/expenses/create`
- **Base URL:** `https://pod01.withmoxie.com/api/public`
- **Official documentation:** [Create Expense](https://help.withmoxie.com/en/articles/8160223-create-expense)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `billNo` | body | `string` | no | Optional bill number for the expense. |
| `category` | body | `string` | no | Optional expense category name. |
| `date` | body | `date` | yes | Expense date. |
| `markupPercentage` | body | `number` | no | Optional markup percentage to apply when the expense is reimbursable. Defaults to 0 to avoid Moxie sample-mode response errors. |
| `notes` | body | `string` | no | Optional notes for the expense. |
| `amount` | body | `number` | yes | Expense amount. |
| `currency` | body | `string` | yes | Expense currency code. |
| `paid` | body | `boolean` | yes | Whether the expense has been paid. |
| `reimbursable` | body | `boolean` | yes | Whether the expense is reimbursable. |
| `vendor` | body | `string` | no | Vendor name for the expense. |
| `clientName` | body | `string` | no | Client name tied to the expense. |
| `description` | body | `string` | no | Expense description. |
