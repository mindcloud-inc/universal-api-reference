# Publish Shifts with RotaCloud

Publishes shifts in RotaCloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/shifts_published`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [Publish Shifts](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shifts[]` | body | `array<number>` | yes | Shift IDs to publish. |
