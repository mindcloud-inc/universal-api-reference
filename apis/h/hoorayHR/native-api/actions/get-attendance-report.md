# Get Attendance Report with HoorayHR

Retrieves an attendance report from HoorayHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/attendance-report`
- **Base URL:** `https://api.hoorayhr.io`
- **Official documentation:** [Get Attendance Report](https://api.hoorayhr.io/documentation/#/attendance-report/findAttendanceReport)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startDate` | query | `string` | yes | The report start date in YYYY-MM-DD format. |
| `endDate` | query | `string` | yes | The report end date in YYYY-MM-DD format. It cannot be more than 31 days after the start date. |
