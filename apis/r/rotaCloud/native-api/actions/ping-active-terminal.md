# Ping Active Terminal with RotaCloud

Pings an active terminal in RotaCloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/terminals_active/:id`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [Ping Active Terminal](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action` | body | `string` | yes | Action payload for terminal ping. |
| `device` | body | `string` | yes | Device identifier for the ping. |
| `id` | path | `number` | yes | Active terminal ID. |
