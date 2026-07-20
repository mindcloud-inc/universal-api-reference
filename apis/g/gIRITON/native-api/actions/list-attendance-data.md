# List Attendance Data with GIRITON

Retrieves configured attendance data from GIRITON.

## Endpoint

- **Method:** `GET`
- **Path:** `/attendance/attendanceData`
- **Base URL:** `https://rest.giriton.com/system/api`
- **Official documentation:** [List Attendance Data](https://rest.giriton.com/apidoc/#/Attendance/getAttendanceData)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dateFrom` | query | `string` | no | Beginning of the attendance time period. |
| `dateTo` | query | `string` | no | End of the attendance time period. |
| `personIds` | query | `string` | no | Comma-separated database IDs of persons. |
