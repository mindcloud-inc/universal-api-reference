# List Time Tracking Import Rows with BambooHR

Lists time tracking import rows from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time-tracking/imports/:id/rows`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Time Tracking Import Rows](https://documentation.bamboohr.com/reference/list-time-tracking-import-rows)

## Requirements

- **OAuth scopes:** `time_tracking:imports`
- **scope:** `time_tracking:imports` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The import ID. |
| `errorsOnly` | query | `boolean` | no | Set to `true` to return only the rows that failed validation. Defaults to `false`, which returns every row. |
