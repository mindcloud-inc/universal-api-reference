# List Time Entries By Employee Id And Date Range with TimeLive

Retrieves time entries from TimeLive by employee and date range.

## Endpoint

- **Method:** `GET`
- **Path:** `/Timesheets/TimeEntriesByEmployeeIdAndDateRange/:employeeId/:startDate/:endDate`
- **Base URL:** `https://mindcloudtl.livetecs.com/classic/api`
- **Official documentation:** [List Time Entries By Employee Id And Date Range](https://livetecs.com/timelive/release-notes/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employeeId` | path | `string` | yes | Account employee id for the time entry range lookup. |
| `endDate` | path | `string` | yes | Range end date in YYYY-MM-DD format. |
| `startDate` | path | `string` | yes | Range start date in YYYY-MM-DD format. |
