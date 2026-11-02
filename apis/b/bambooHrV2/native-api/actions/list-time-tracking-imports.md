# List Time Tracking Imports with BambooHR

Lists time tracking imports from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time-tracking/imports`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Time Tracking Imports](https://documentation.bamboohr.com/reference/list-time-tracking-imports)

## Requirements

- **OAuth scopes:** `time_tracking:imports`
- **scope:** `time_tracking:imports` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `list<string>` | no | Restrict the results to one status. Omit to return both `DRAFT` and `COMPLETE` imports. Accepted values: `COMPLETE`, `DRAFT`. |
