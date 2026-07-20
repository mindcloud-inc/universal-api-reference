# Create Shift with RotaCloud

Creates a shift in RotaCloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/shifts`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [Create Shift](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end_time` | body | `number` | yes | Shift end time as a Unix timestamp. |
| `location` | body | `number` | yes | Location ID for the shift. |
| `start_time` | body | `number` | yes | Shift start time as a Unix timestamp. |
