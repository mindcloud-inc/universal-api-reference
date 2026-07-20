# Add Layer Overrides with Statsig

Adds layer overrides in Statsig.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/console/v1/layers/{id}/overrides`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Add Layer Overrides](https://docs.statsig.com/api-reference/layers/add-layer-overrides)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `op` | body | `string` | yes | Request body field. |
| `conditionalOverrides` | body | `list` | yes | Request body field. |
| `idOverrides` | body | `list` | yes | Request body field. |
