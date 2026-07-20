# Delete Attendance Event with GIRITON

Deletes an attendance event from GIRITON.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/attendance/attendanceEvent`
- **Base URL:** `https://rest.giriton.com/system/api`
- **Official documentation:** [Delete Attendance Event](https://rest.giriton.com/apidoc/#/Attendance/removeAttendanceEvent)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attendanceEventId` | body | `string` | yes | Attendance event ID to delete. |
