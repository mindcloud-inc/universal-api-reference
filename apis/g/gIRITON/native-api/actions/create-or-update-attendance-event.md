# Create Or Update Attendance Event with GIRITON

Creates or updates an attendance event in GIRITON.

## Endpoint

- **Method:** `POST`
- **Path:** `/attendance/attendanceEvent`
- **Base URL:** `https://rest.giriton.com/system/api`
- **Official documentation:** [Create Or Update Attendance Event](https://rest.giriton.com/apidoc/#/Attendance/addAttendanceEventJsonBody)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | body | `string` | no | User ID for the attendance event. |
| `attendanceActivityId` | body | `string` | no | Attendance activity ID for the event. |
| `dateTime` | body | `string` | no | Date time of the attendance event, for example 2026-04-30T09:00+02:00. |
| `startOrStop` | body | `boolean` | yes | Whether the attendance activity starts or stops at the given date time. |
| `note` | body | `string` | no | Optional attendance event note. |
