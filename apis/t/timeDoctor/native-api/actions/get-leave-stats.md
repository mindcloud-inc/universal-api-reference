# Get Leave Stats with Time Doctor

Retrieves leave stats from Time Doctor.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/1.0/work-schedules/stats`
- **Base URL:** `https://api2.timedoctor.com`
- **Official documentation:** [Get Leave Stats](https://api2.timedoctor.com/#operation/getLeaveStats)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `from` | query | `string` | yes |
| `to` | query | `string` | yes |
