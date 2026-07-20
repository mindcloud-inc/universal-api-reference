# Update Shifts Batch with RotaCloud

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/shifts`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [Update Shifts Batch](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shifts[]` | body | `array<object>` | yes | Shift records to update in batch. |
