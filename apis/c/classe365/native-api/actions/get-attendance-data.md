# Get Attendance Data with Classe365

Retrieves attendance data for students from Classe365.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/attendanceData`
- **Base URL:** `https://{username}.classe365.com`
- **Official documentation:** [Get Attendance Data](https://speca.io/classe365/academics#get-attendance-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `acds_id` | query | `string` | no | Academic session id. |
| `class_id` | query | `string` | no | Class id. |
| `date` | query | `string` | no | Attendance date in YYYY-MM-DD. |
| `section_id` | query | `string` | no | Section id. |
| `session_id` | query | `string` | no | Session id when multiple sessions are enabled. |
| `subject_id` | query | `string` | no | Subject id for subject-wise attendance. |
