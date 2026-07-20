# Get Person Attendance Data with GIRITON

Retrieves configured attendance data for one GIRITON person.

## Endpoint

- **Method:** `GET`
- **Path:** `/attendance/personAttendanceData`
- **Base URL:** `https://rest.giriton.com/system/api`
- **Official documentation:** [Get Person Attendance Data](https://rest.giriton.com/apidoc/#/Attendance/getPersonAttendanceData)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `personId` | query | `string` | no | ID of the required person. |
| `personNumber` | query | `string` | no | Person number of the required person. |
| `dateFrom` | query | `string` | no | Beginning of the attendance time period. |
| `dateTo` | query | `string` | no | End of the attendance time period. |
