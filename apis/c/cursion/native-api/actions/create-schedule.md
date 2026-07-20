# Create Schedule with Cursion

## Endpoint

- **Method:** `POST`
- **Path:** `/schedule`
- **Base URL:** `https://api.cursion.dev/v1/ops`
- **Official documentation:** [Create Schedule](https://docs.cursion.dev/api/schedule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `begin_date` | body | `string` | yes | The date to start the schedule. |
| `frequency` | body | `string` | yes | How often the schedule runs. |
| `site_id` | body | `string` | yes | The site identifier to schedule. |
| `task_type` | body | `string` | yes | The scheduled task type: scan, test, or report. |
| `time` | body | `string` | yes | The 24-hour time to run the schedule. |
| `timezone` | body | `string` | yes | The IANA timezone for the schedule. |
