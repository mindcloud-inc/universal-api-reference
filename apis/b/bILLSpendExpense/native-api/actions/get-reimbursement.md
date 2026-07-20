# Get Reimbursement with BILL Spend & Expense

Retrieves a reimbursement from BILL Spend & Expense.

## Endpoint

- **Method:** `GET`
- **Path:** `spend/reimbursements/:reimbursementId`
- **Base URL:** `https://gateway.{environment}.bill.com/connect/v3`
- **Official documentation:** [Get Reimbursement](https://developer.bill.com/reference/getreimbursement)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reimbursementId` | path | `list` | yes | BILL-generated ID or UUID of the reimbursement. |
