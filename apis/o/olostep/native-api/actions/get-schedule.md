# Get Schedule with Olostep

Retrieves details for a schedule in Olostep.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/schedules/[:schedule_id]`
- **Base URL:** `https://api.olostep.com`
- **Official documentation:** [Get Schedule](https://docs.olostep.com/api-reference/schedules/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `schedule_id` | path | `string` | yes | Unique schedule identifier. Olostep schedule IDs start with `schedule_`. |
