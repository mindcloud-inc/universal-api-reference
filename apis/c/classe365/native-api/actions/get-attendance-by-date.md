# Get Attendance by Date with Classe365

Retrieves attendance data from Classe365 for a specific date.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/allAttendanceByDate`
- **Base URL:** `https://{username}.classe365.com`
- **Official documentation:** [Get Attendance by Date](https://speca.io/classe365/academics#get-all-attendance-data-for-particular-date)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `acds_id` | query | `string` | no | Academic session id. |
| `date` | query | `string` | no | Attendance date in YYYY-MM-DD. |
