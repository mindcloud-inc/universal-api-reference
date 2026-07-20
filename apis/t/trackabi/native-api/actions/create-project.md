# Create Project with Trackabi

Creates a new project in Trackabi.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/projects`
- **Base URL:** `https://api.trackabi.com`
- **Official documentation:** [Create Project](https://trackabi.com/help/api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | — |
| `client_id` | body | `number` | no | Required if the client column is mandatory according to the timesheet settings. |
| `short_name` | body | `string` | yes | — |
| `description` | body | `string` | no | — |
| `start_date` | body | `date` | no | — |
| `end_date` | body | `date` | no | — |
| `hourly_rate` | body | `number` | no | Cost hourly rate (access-restricted). |
| `cost_hourly_rate` | body | `number` | no | Project currency rate (access-restricted). |
| `currency` | body | `string` | yes | Project currency. |
| `estimate_units` | body | `string` | no | Estimate units of the project. |
| `not_billable` | body | `number` | no | Set to 1 or 0. |
