# Get Employment Report with Leave Dates

Retrieves employment report rows from Leave Dates.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/employments`
- **Base URL:** `https://api.leavedates.com`
- **Official documentation:** [Get Employment Report](https://api.leavedates.com/documentation#/Reporting/get_reports_employments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | query | `string` | yes | Company ID |
| `department` | query | `string` | no | Department ID |
| `report_type` | query | `string` | no | Selected type of the report |
