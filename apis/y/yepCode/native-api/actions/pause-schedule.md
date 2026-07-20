# Pause scheduled process with YepCode

Updates a scheduled process in YepCode by pausing it.

## Endpoint

- **Method:** `PUT`
- **Path:** `/schedules/:id/pause`
- **Base URL:** `https://cloud.yepcode.io/api/{team}/rest`
- **Official documentation:** [Pause scheduled process](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Schedules/pauseSchedule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier of the scheduled process to pause. |
