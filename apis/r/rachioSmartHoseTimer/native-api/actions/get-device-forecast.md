# Get Device Forecast with Rachio Smart Hose Timer

Retrieves a device forecast from Rachio.

## Endpoint

- **Method:** `GET`
- **Path:** `/public/device/:id/forecast`
- **Base URL:** `https://api.rach.io/1`
- **Official documentation:** [Get Device Forecast](https://rachio.readme.io/reference/publicdeviceidforecastunitsunits)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Device's unique id |
| `units` | query | `string` | yes | Forecast units: US or METRIC |
