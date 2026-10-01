# Create Budget with QuickBooks Online

## Endpoint

- **Method:** `POST`
- **Path:** `/budget`
- **Base URL:** `https://:quickbooksEnvironment/v3/company/:realmId`
- **Official documentation:** [Create Budget](https://developer.intuit.com/app/developer/qbo/docs/api/accounting/all-entities/budget)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Name` | body | `string` | yes | Budget name. |
| `StartDate` | body | `date` | yes | Budget start date. |
| `EndDate` | body | `date` | yes | Budget end date. |
| `BudgetType` | body | `string` | yes | QuickBooks budget type. Production proof used ProfitAndLoss. |
| `BudgetEntryType` | body | `string` | yes | QuickBooks budget entry cadence. Production proof used Monthly. |
| `Active` | body | `boolean` | no | Whether the budget is active. |
