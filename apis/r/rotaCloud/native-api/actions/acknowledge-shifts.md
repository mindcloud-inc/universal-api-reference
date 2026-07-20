# Acknowledge Shifts with RotaCloud

Acknowledges shifts in RotaCloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/shifts_acknowledged`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [Acknowledge Shifts](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shifts[]` | body | `array<number>` | yes | Shift IDs to acknowledge. |
