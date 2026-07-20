# Add Reimbursement Receipt with BILL Spend & Expense

Adds a receipt to a reimbursement in BILL Spend & Expense.

## Endpoint

- **Method:** `POST`
- **Path:** `spend/reimbursements/:reimbursementId/receipts`
- **Base URL:** `https://gateway.{environment}.bill.com/connect/v3`
- **Official documentation:** [Add Reimbursement Receipt](https://developer.bill.com/reference/addreimbursementreceipt)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filename` | body | `string` | yes | Receipt file name. |
| `reimbursementId` | path | `list` | yes | BILL-generated ID or UUID of the reimbursement. |
| `url` | body | `string` | yes | Uploaded receipt URL returned by the reimbursement upload URL flow. |
