# List Payroll Timesheets with ServiceTitan

Retrieves payroll job timesheets from ServiceTitan.

## Endpoint

- **Method:** `GET`
- **Path:** `payroll/v2/tenant/{tenant}/jobs/timesheets`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [List Payroll Timesheets](https://developer.servicetitan.io/api-details/#api=tenant-payroll-v2&operation=Timesheets_GetJobTimesheetsByJobs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `technicianId` | query | `number` | no |
| `active` | query | `list` | no |
| `pageSize` | query | `number` | no |
| `modifiedOnOrAfter` | query | `string` | no |
| `endedOn` | query | `string` | no |
| `jobIds` | query | `string` | no |
| `startedOn` | query | `string` | no |
