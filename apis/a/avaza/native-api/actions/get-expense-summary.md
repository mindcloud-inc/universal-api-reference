# Get Expense Summary with Avaza

Retrieves aggregated expense data from Avaza.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/ExpenseSummary`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [Get Expense Summary](https://api.avaza.com/#!/ExpenseSummary/ExpenseSummary_Get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model.groupBy` | query | `list<string>` | no | (Optional) Combine one, two or three levels of Grouping. Combine these possible grouping values: "Category", "ChargeableStatus", "Merchant", "ApprovalStatus", "ReimbursementStatus", "Customer", "Project", "User", "Task", "Year", "Month", "Day", "Week". |
| `model.expenseDateFrom` | query | `date` | no | (Required) Filter for expenses with expense dates greater or equal to the specified date. e.g. 2019-01-25. |
| `model.expenseDateTo` | query | `date` | no | (Required) Filter for expenses with an expense date smaller or equal to the specified  date. e.g. 2019-01-25. |
| `model.userID` | query | `list<number>` | no | (Optional) Defaults to the current user. Provide one or more UserIDs of Users whose expenses should be retrieved. If the current user doesn't have impersonation rights, then they will only see their own data. |
| `model.projectID` | query | `number` | no | (Optional) Filter by Project |
