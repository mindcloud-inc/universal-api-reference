# Get Time Tracking Shift Differential with BambooHR

Retrieves time tracking shift differential from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time-tracking/shift-differentials/:id`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Time Tracking Shift Differential](https://documentation.bamboohr.com/reference/get-shift-differential)

## Requirements

- **OAuth scopes:** `time_tracking:shift_differentials`
- **scope:** `time_tracking:shift_differentials` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The shift differential ID. |
