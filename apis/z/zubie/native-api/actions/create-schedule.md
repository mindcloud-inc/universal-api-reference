# Create Schedule with Zubie

Creates a schedule in Zubie.

## Endpoint

- **Method:** `POST`
- **Path:** `/schedules`
- **Base URL:** `https://api.zubiecar.com/api/v2/zinc`
- **Official documentation:** [Create Schedule](https://developer.zubie.com/reference/schedules)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `periods[]` | body | `array<object>` | yes | List of schedule periods. |
