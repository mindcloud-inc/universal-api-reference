# List Expenses with Avaza

Retrieves expenses from Avaza.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/Expense`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [List Expenses](https://api.avaza.com/#!/Expense/Expense_Get)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `UpdatedAfter` | query | `date` | no |
| `ExpenseDateFrom` | query | `date` | no |
| `ExpenseDateTo` | query | `date` | no |
| `UserEmail` | query | `string` | no |
| `UserID` | query | `number` | no |
| `CategoryName` | query | `string` | no |
| `CustomerID` | query | `number` | no |
| `ProjectID` | query | `number` | no |
| `isChargeable` | query | `boolean` | no |
| `isInvoiced` | query | `boolean` | no |
| `ExpenseReimbursementIDFK` | query | `number` | no |
| `ExpensePaymentMethodIDFK` | query | `number` | no |
| `ExpenseApprovalStatusCode` | query | `string` | no |
| `Search` | query | `string` | no |
