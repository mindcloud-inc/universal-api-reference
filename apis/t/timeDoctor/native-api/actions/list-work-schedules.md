# List Work Schedules with Time Doctor

Retrieves work schedules from Time Doctor.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/1.0/work-schedules`
- **Base URL:** `https://api2.timedoctor.com`
- **Official documentation:** [List Work Schedules](https://api2.timedoctor.com/#operation/getWorkSchedules)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `from` | query | `string` | yes |
| `to` | query | `string` | yes |
