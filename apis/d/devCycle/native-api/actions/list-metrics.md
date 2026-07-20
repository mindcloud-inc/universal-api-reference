# List Metrics with DevCycle

Retrieves metrics from DevCycle.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project/metrics`
- **Base URL:** `https://api.devcycle.com`
- **Official documentation:** [List Metrics](https://docs.devcycle.com/management-api/#tag/Metrics/operation/MetricsController_findAll)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | path | `string` | no | Project key. |
