# Update Availability with RotaCloud

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/availability`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [Update Availability](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user` | body | `number` | yes | User ID for the availability pattern. |
| `dates[]` | body | `array<object>` | yes | Availability date objects. |
