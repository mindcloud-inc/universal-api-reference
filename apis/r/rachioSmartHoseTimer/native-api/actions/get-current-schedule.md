# Get Current Schedule with Rachio Smart Hose Timer

Retrieves the current schedule from Rachio.

## Endpoint

- **Method:** `GET`
- **Path:** `/public/device/:id/current_schedule`
- **Base URL:** `https://api.rach.io/1`
- **Official documentation:** [Get Current Schedule](https://rachio.readme.io/reference/publicdeviceidcurrent_schedule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Controller device UUID. |
