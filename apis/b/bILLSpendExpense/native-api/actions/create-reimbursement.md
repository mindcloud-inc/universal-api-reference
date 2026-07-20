# Create Reimbursement with BILL Spend & Expense

Creates a new reimbursement in BILL Spend & Expense.

## Endpoint

- **Method:** `POST`
- **Path:** `spend/reimbursements`
- **Base URL:** `https://gateway.{environment}.bill.com/connect/v3`
- **Official documentation:** [Create Reimbursement](https://developer.bill.com/reference/createreimbursement)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | body | `number` | yes | Reimbursement amount. |
| `budgetId` | body | `list` | yes | BILL-generated ID of the budget used for the reimbursement. |
| `customFields[]` | body | `array<object>` | no | Custom field objects and values for the reimbursement. |
| `merchantName` | body | `string` | yes | Merchant name for the expense. |
| `note` | body | `string` | yes | Business purpose for the expense. |
| `occurredDate` | body | `string` | yes | Expense date in yyyy-MM-dd format, for example 2026-10-15. |
| `userId` | body | `list` | yes | BILL-generated ID of the user to be reimbursed. |
| `receiptUrl` | body | `string` | yes | Use the upload URL returned by Create Reimbursement Upload URL after uploading the JPG or PNG receipt image to that URL. |
| `receiptFilename` | body | `string` | yes | Receipt file name with extension, for example receipt.jpg or receipt.png. BILL stores this together with the uploaded receipt URL. |
