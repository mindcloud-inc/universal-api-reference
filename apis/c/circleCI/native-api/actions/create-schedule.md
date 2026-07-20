# Create Schedule with CircleCI

## Endpoint

- **Method:** `POST`
- **Path:** `/project/:project_slug/schedule`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Create Schedule](https://circleci.com/docs/api/v2/#tag/Schedule/operation/createSchedule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attribution-actor` | body | `string` | no | Actor to attribute schedule-triggered pipelines to. |
| `description` | body | `string` | no | Schedule description. |
| `name` | body | `string` | no | Schedule name. |
| `parameters` | body | `object` | no | Pipeline parameters to send when the schedule runs. |
| `project_slug` | path | `string` | no | Project slug in the form vcs/org/repo. |
| `timetable` | body | `object` | no | Schedule timetable definition. |
