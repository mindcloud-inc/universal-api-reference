# Launch Active Terminal with RotaCloud

Launches a terminal in RotaCloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/terminals_active`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [Launch Active Terminal](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `device` | body | `string` | yes | Device name or identifier. |
| `terminal` | body | `number` | yes | Terminal ID to launch. |
