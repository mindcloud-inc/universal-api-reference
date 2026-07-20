# Unpublish Shifts with RotaCloud

Unpublishes shifts in RotaCloud.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/shifts_published`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [Unpublish Shifts](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shifts[]` | body | `array<number>` | yes | Shift IDs to unpublish. |
