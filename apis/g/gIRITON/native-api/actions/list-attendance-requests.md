# List Attendance Requests with GIRITON

Retrieves a list of attendance requests from GIRITON.

## Endpoint

- **Method:** `GET`
- **Path:** `/requests/requests`
- **Base URL:** `https://rest.giriton.com/system/api`
- **Official documentation:** [List Attendance Requests](https://rest.giriton.com/apidoc/#/Attendance%20requests/getAttendanceRequests)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requestStates` | query | `string` | no | Comma-separated request states such as new, approved, refused, deleted, or all. |
| `requestTypes` | query | `string` | no | Comma-separated request types such as attendance_new, attendance_change, shift, or all. |
| `dateFrom` | query | `string` | no | Start date of the request period. |
| `dateTo` | query | `string` | no | End date of the request period. |
