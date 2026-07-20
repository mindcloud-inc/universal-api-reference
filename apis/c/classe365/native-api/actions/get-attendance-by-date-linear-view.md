# Get Attendance by Date (Linear View) with Classe365

Retrieves attendance data in linear view from Classe365.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/attendanceByDateInLV`
- **Base URL:** `https://{username}.classe365.com`
- **Official documentation:** [Get Attendance by Date (Linear View)](https://speca.io/classe365/academics#get-attendance-date-for-all-students-and-particular-date-in-linear-view)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `acds_id` | query | `string` | no | Academic session id. |
| `date` | query | `string` | no | Attendance date in YYYY-MM-DD. |
