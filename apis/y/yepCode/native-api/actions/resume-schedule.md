# Resume scheduled process with YepCode

Updates a scheduled process in YepCode by resuming it.

## Endpoint

- **Method:** `PUT`
- **Path:** `/schedules/:id/resume`
- **Base URL:** `https://cloud.yepcode.io/api/{team}/rest`
- **Official documentation:** [Resume scheduled process](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Schedules/resumeSchedule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier of the scheduled process to resume. |
