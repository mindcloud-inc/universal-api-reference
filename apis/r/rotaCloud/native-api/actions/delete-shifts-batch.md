# Delete Shifts Batch with RotaCloud

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/shifts`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [Delete Shifts Batch](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | body | `array<number>` | yes | Shift IDs to delete in batch. |
