# Update Layer Overrides with Statsig

Updates layer overrides in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/layers/{id}/overrides`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Update Layer Overrides](https://docs.statsig.com/api-reference/layers/update-layer-overrides)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `conditionalOverrides` | body | `list` | yes | Request body field. |
| `idOverrides` | body | `list` | yes | Request body field. |
