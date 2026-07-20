# Update Schedule with Zubie

Updates an existing schedule in Zubie.

## Endpoint

- **Method:** `POST`
- **Path:** `/schedule/{schedule_key}`
- **Base URL:** `https://api.zubiecar.com/api/v2/zinc`
- **Official documentation:** [Update Schedule](https://developer.zubie.com/reference/schedules)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `periods[]` | body | `array<object>` | yes | List of schedule periods. |
| `schedule_key` | path | `string` | yes | Unique schedule key. |
