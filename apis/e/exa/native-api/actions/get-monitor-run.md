# Get Monitor Run with Exa

Retrieves a monitor run from Exa.

## Endpoint

- **Method:** `GET`
- **Path:** `/monitors/:id/runs/:runId`
- **Base URL:** `https://api.exa.ai`
- **Official documentation:** [Get Monitor Run](https://exa.ai/docs/websets/api/monitors/runs/get-monitor-run)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Monitor identifier. |
| `runId` | path | `string` | yes | Run identifier. |
