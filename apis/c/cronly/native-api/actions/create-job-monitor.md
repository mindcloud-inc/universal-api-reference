# Create Job Monitor with Cronly

## Endpoint

- **Method:** `POST`
- **Path:** `/api/monitors`
- **Base URL:** `https://cronly.app`
- **Official documentation:** [Create Job Monitor](https://docs.cronly.app/api/cron-job-monitor-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the job monitor. |
| `timezone` | body | `string` | yes | Timezone for the monitor schedule. |
| `project_id` | body | `number` | no | Optional project to associate with the monitor. |
| `schedule` | body | `string` | yes | Cron schedule for the monitor. |
| `duration` | body | `number` | yes | Allowed duration in minutes. |
