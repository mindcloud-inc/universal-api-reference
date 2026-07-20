# Get scheduled process with YepCode

Retrieves a scheduled process from YepCode.

## Endpoint

- **Method:** `GET`
- **Path:** `/schedules/:id`
- **Base URL:** `https://cloud.yepcode.io/api/{team}/rest`
- **Official documentation:** [Get scheduled process](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Schedules/getSchedule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier of the scheduled process to retrieve. |
