# Get Time Tracking Import Row with BambooHR

Retrieves time tracking import row from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time-tracking/imports/:id/rows/:rowId`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Time Tracking Import Row](https://documentation.bamboohr.com/reference/get-time-tracking-import-row)

## Requirements

- **OAuth scopes:** `time_tracking:imports`
- **scope:** `time_tracking:imports` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The import ID. |
| `rowId` | path | `number` | yes | The import row ID. |
