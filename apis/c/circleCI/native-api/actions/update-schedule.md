# Update Schedule with CircleCI

## Endpoint

- **Method:** `PATCH`
- **Path:** `/schedule/:schedule_id`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Update Schedule](https://circleci.com/docs/api/v2/#tag/Schedule/operation/updateSchedule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attribution-actor` | body | `string` | no | Actor to attribute schedule-triggered pipelines to. |
| `description` | body | `string` | no | Schedule description. |
| `name` | body | `string` | no | Schedule name. |
| `parameters` | body | `object` | no | Pipeline parameters to send when the schedule runs. |
| `schedule_id` | path | `string` | no | Opaque schedule identifier. |
| `timetable` | body | `object` | no | Schedule timetable definition. |
