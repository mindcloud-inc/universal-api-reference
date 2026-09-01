# List Center Employee Schedules with Zenoti

## Endpoint

- **Method:** `GET`
- **Path:** `centers/:centerId/employee_schedules`
- **Base URL:** `https://api.zenoti.com/v1/`
- **Official documentation:** [List Center Employee Schedules](https://docs.zenoti.com/reference/retrieve-the-schedules-of-employees-of-a-center)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `centerId` | path | `list` | no | — |
| `start_date` | query | `date` | no | — |
| `end_date` | query | `date` | no | — |
| `schedule_status` | query | `list` | no | — |
| `employee_id` | query | `string` | no | — |
| `consider_schedule_time` | query | `boolean` | no | If true, the API considers the time stamp for the specified date range to filter the response data. If false, the API considers only the date values to filter the employee schedules. |
