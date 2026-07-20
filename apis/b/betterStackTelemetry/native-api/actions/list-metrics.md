# List Metrics with Better Stack Telemetry

Retrieves metrics for a source from Better Stack Telemetry.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/sources/:source_id/metrics`
- **Base URL:** `https://telemetry.betterstack.com`
- **Official documentation:** [List Metrics](https://betterstack.com/docs/logs/api/list-all-existing-metrics/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source_id` | path | `string` | yes | Source for which to retrieve metrics |
