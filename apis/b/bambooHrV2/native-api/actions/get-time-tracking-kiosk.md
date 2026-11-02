# Get Time Tracking Kiosk with BambooHR

Retrieves time tracking kiosk from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time-tracking/kiosks/:id`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Time Tracking Kiosk](https://documentation.bamboohr.com/reference/get-time-tracking-kiosk)

## Requirements

- **OAuth scopes:** `time_tracking:kiosks`
- **scope:** `time_tracking:kiosks` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The time tracking kiosk ID. |
