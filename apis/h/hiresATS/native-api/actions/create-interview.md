# Create Interview with 100Hires ATS

Schedules an interview for an application in 100Hires ATS.

## Endpoint

- **Method:** `POST`
- **Path:** `/applications/:id/interviews`
- **Base URL:** `https://api.100hires.com/v2`
- **Official documentation:** [Create Interview](https://100hires.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Application ID to attach the interview to. |
| `start_time` | body | `number` | yes | Interview start time as a Unix timestamp in seconds. |
| `end_time` | body | `number` | yes | Interview end time as a Unix timestamp in seconds. |
| `interviewer_ids[]` | body | `array<number>` | yes | User IDs for the interviewers. |
| `location` | body | `string` | no | Optional interview location string. |
| `include` | query | `string` | no | Comma-separated related interview resources to include. |
