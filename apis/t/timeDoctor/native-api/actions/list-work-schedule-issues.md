# List Work Schedule Issues with Time Doctor

Retrieves work schedule issues from Time Doctor.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/1.0/work-schedules/issues`
- **Base URL:** `https://api2.timedoctor.com`
- **Official documentation:** [List Work Schedule Issues](https://api2.timedoctor.com/#operation/getWorkSchedulesIssues)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `from` | query | `string` | yes |
| `to` | query | `string` | yes |
