# Upsert Attendance with Classe365

Creates or updates attendance in Classe365.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/manageAttendance`
- **Base URL:** `https://{username}.classe365.com`
- **Official documentation:** [Upsert Attendance](https://speca.io/classe365/academics#attendance)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `acds_id` | body | `string` | no | Academic session id. |
| `attendance_data` | body | `string` | no | JSON map of student attendance values. |
| `class_id` | body | `string` | no | Class id. |
| `date` | body | `string` | no | Attendance date in YYYY-MM-DD. |
| `section_id` | body | `string` | no | Section id. |
| `session_id` | body | `string` | no | Session id. |
| `subject_id` | body | `string` | no | Subject id. |
| `working` | body | `string` | no | 1 for working day. |
