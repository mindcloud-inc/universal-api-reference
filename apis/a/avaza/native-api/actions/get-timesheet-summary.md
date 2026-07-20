# Get Timesheet Summary with Avaza

Retrieves aggregated timesheet data from Avaza.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/TimesheetSummary`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [Get Timesheet Summary](https://api.avaza.com/#!/TimesheetSummary/TimesheetSummary_Get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model.groupBy` | query | `list<string>` | no | (Optional) Combine one, two or three levels of Grouping. Combine these possible grouping values: "Customer", "Project", "Category", "User", "Task", "Year", "Month", "Day", "Week". |
| `model.entryDateFrom` | query | `date` | no | (Required) Filter for timesheets greater or equal to the specified date. e.g. 2019-01-25. You can optionally include a time component, otherwise it assumes 00:00 |
| `model.entryDateTo` | query | `date` | no | (Required) Filter for timesheets with an entry date smaller or equal to the specified  date. e.g. 2019-01-25. You can optionally include a time component, otherwise it assumes 00:00 |
| `model.userID` | query | `list<number>` | no | (Optional) Defaults to the current user. Provide one or more UserIDs of Users whose timesheets should be retrieved. If the current user doesn't have impersonation rights, then they will only see their own data. |
| `model.projectID` | query | `number` | no | (Optional) Filter by Project |
| `model.isBillable` | query | `boolean` | no | (Optional) Filter by the billable status of Timesheets. |
| `model.isInvoiced` | query | `boolean` | no | (Optional) Filter for timesheets by whether they have been Invoiced or not. |
| `model.timesheetEntryApprovalStatusCode` | query | `list<string>` | no | (Optional) Filter for timesheets that belong to one of the specified statuses (Draft, Pending, Approved, AutoApproved, Rejected) |
