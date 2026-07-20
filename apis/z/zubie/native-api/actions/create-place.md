# Create Place with Zubie

Creates a place in Zubie.

## Endpoint

- **Method:** `POST`
- **Path:** `/places`
- **Base URL:** `https://api.zubiecar.com/api/v2/zinc`
- **Official documentation:** [Create Place](https://developer.zubie.com/reference/places)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active_weekdays[]` | body | `array<number>` | yes | Days of week to detect geofence events. |
| `from_time` | body | `string` | yes | Start time window in hh:mm format. |
| `to_time` | body | `string` | yes | End time window in hh:mm format. |
