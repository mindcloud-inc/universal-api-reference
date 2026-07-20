# Disable Lost Mode with Universal API

Disables lost mode for a device in Universal API.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/mdm/devices/{id}/lost-mode/disable`
- **Base URL:** `https://api.prod.universalapi.io`
- **Official documentation:** [Disable Lost Mode](https://docs.universalapi.io/reference/disable-lost-mode)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Device ID. |
