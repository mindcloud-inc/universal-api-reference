# Load Pulse (Warehouse Native) with Statsig

Loads a warehouse-native pulse in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/experiments/{id}/load_pulse`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Load Pulse (Warehouse Native)](https://docs.statsig.com/api-reference/experiments/load-pulse-warehouse-native)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `refresh` | query | `string` | no | — |
| `metricIDs` | query | `list` | no | — |
| `turboMode` | query | `boolean` | no | — |
