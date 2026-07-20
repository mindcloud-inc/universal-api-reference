# Submit Expenses for Approval with Avaza

Submits expenses for approval in Avaza.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/ExpenseApproval/Submit`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [Submit Expenses for Approval](https://api.avaza.com/#!/Expense/ExpenseApproval)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `UserID` | query | `number` | no | The user to submit the Expenses for. Defaults to current user. Only allowed to be different from the current user when the current user has rights to Impersonate other users. |
| `SendNotifications` | query | `boolean` | no | Send email alerts to expense approvers. Defaults to true |
