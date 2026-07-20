# Update Job Schedule with Housecall Pro

## Endpoint

- **Method:** `PUT`
- **Path:** `/jobs/:job_id/schedule`
- **Base URL:** `https://api.housecallpro.com`
- **Official documentation:** [Update Job Schedule](https://docs.housecallpro.com/docs/housecall-public-api/1d344f58672f9-update-job-schedule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | yes | The ID of the job. |
| `start_time` | body | `date` | yes | Start time of the job in ISO-8601 format. |
| `end_time` | body | `date` | no | End time of the job in ISO-8601 format. |
| `arrival_window_in_minutes` | body | `number` | no | Arrival window in minutes. |
| `notify` | body | `boolean` | no | Notify the customer of the schedule update. |
| `notify_pro` | body | `boolean` | no | Notify the employee of the schedule update. |
| `expand[]` | body | `array<string>` | no | Additional fields to expand in the response. |
| `dispatched_employees[]` | body | `array<object>` | no | Dispatched employees payload. |
