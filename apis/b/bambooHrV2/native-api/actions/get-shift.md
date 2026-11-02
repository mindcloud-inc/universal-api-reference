# Get Shift with BambooHR

Retrieves shift from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/scheduling/shifts/:id`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Shift](https://documentation.bamboohr.com/reference/scheduling-get-shift)

## Requirements

- **OAuth scopes:** `scheduling:shifts time_tracking`
- **scope:** `scheduling:shifts, time_tracking` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The shift uuid |
