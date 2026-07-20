# List Monitor Runs with Exa

Retrieves monitor runs from Exa.

## Endpoint

- **Method:** `GET`
- **Path:** `/monitors/:id/runs`
- **Base URL:** `https://api.exa.ai`
- **Official documentation:** [List Monitor Runs](https://exa.ai/docs/websets/api/monitors/runs/list-monitor-runs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Monitor identifier. |
