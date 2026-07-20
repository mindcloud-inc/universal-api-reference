# Delete Availability with RotaCloud

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/availability`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [Delete Availability](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user` | body | `number` | yes | User ID for the availability deletion. |
| `dates[]` | body | `array<object>` | yes | Availability dates to clear. |
