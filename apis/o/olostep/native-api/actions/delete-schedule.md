# Delete Schedule with Olostep

Deletes an existing schedule from Olostep.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/schedules/[:schedule_id]`
- **Base URL:** `https://api.olostep.com`
- **Official documentation:** [Delete Schedule](https://docs.olostep.com/api-reference/schedules/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `schedule_id` | path | `string` | yes | Unique identifier for the schedule to delete. Must start with `schedule_`. |
