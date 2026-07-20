# List Device Webhooks with Rachio Smart Hose Timer

Retrieves webhooks for a specific Rachio device.

## Endpoint

- **Method:** `GET`
- **Path:** `/public/notification/:deviceId/webhook`
- **Base URL:** `https://api.rach.io/1`
- **Official documentation:** [List Device Webhooks](https://rachio.readme.io/reference/publicnotificationdeviceidwebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deviceId` | path | `string` | yes | Controller device UUID. |
