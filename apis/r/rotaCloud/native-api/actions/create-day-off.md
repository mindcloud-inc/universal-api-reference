# Create Day Off with RotaCloud

Creates days off in RotaCloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/days_off`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [Create Day Off](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dates[]` | body | `array<object>` | yes | Array of day-off date objects. |
| `user` | body | `number` | yes | User ID for the day off. |
