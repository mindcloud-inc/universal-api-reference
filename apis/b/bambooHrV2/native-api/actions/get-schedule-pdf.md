# Get Schedule PDF with BambooHR

Retrieves schedule pdf from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/scheduling/schedules/:id/pdf`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Schedule PDF](https://documentation.bamboohr.com/reference/scheduling-get-schedule-pdf)

## Requirements

- **OAuth scopes:** `scheduling:schedules`
- **scope:** `scheduling:schedules` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The schedule ID |
| `startYmd` | query | `date` | yes | Start date in YYYY-MM-DD format Format: `YYYY-MM-DD`. |
| `endYmd` | query | `date` | yes | End date in YYYY-MM-DD format Format: `YYYY-MM-DD`. |
| `groupBy` | query | `list<string>` | no | Group employees by this field Accepted values: `department`, `division`, `jobTitle`, `location`, `team`. |
| `employeeIds[]` | query | `string` | no | Filter by employee IDs. Pass the string "null" as an element to include open shifts. Send multiple values as a array. |
| `includeEmployeesWithoutShifts` | query | `boolean` | no | Whether to include employees who have no shifts in the date range |
| `includeHolidays` | query | `boolean` | no | Whether to include holidays in the PDF |
| `includeTimeOff` | query | `boolean` | no | Whether to include time-off entries in the PDF |
