# Get Time Tracking Configuration with BambooHR

Retrieves time tracking configuration from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time-tracking/configurations/:id`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Time Tracking Configuration](https://documentation.bamboohr.com/reference/get-time-tracking-configuration)

## Requirements

- **OAuth scopes:** `time_tracking:configurations`
- **scope:** `time_tracking:configurations` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The configuration ID. |
