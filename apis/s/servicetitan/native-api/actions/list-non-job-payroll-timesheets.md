# List Non-Job Payroll Timesheets with ServiceTitan

Retrieves non-job payroll timesheets from ServiceTitan.

## Endpoint

- **Method:** `GET`
- **Path:** `payroll/v2/tenant/{tenant}/non-job-timesheets`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [List Non-Job Payroll Timesheets](https://developer.servicetitan.io/api-details/#api=tenant-payroll-v2&operation=Timesheets_GetNonJobTimesheets)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `active` | query | `list` | no |
| `employeeId` | query | `number` | no |
| `pageSize` | query | `number` | no |
| `employeeType` | query | `list` | no |
| `createdBefore` | query | `string` | no |
| `createdOnOrAfter` | query | `string` | no |
| `modifiedOnOrAfter` | query | `string` | no |
