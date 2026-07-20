# Load Pulse Gate with Statsig

Loads a pulse gate in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/gates/{id}/load_pulse`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Load Pulse Gate](https://docs.statsig.com/api-reference/gates/load-pulse-gate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `refresh` | body | `string` | no | Request body field. |
| `metricIDs` | body | `list` | no | Request body field. |
| `ruleId` | body | `string` | yes | Request body field. |
| `turboMode` | body | `boolean` | no | Request body field. |
