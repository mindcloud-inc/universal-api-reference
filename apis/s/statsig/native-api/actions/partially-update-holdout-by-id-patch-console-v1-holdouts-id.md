# Partially update holdout by id with Statsig

Updates a holdout in Statsig by ID.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/console/v1/holdouts/{id}`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Partially update holdout by id](https://docs.statsig.com/api-reference/holdouts/partially-update-holdout-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `isEnabled` | body | `boolean` | no | Request body field. |
| `description` | body | `string` | no | Request body field. |
| `passPercentage` | body | `number` | no | Request body field. |
| `gateIDs` | body | `list` | no | Request body field. |
| `experimentIDs` | body | `list` | no | Request body field. |
| `layerIDs` | body | `list` | no | Request body field. |
| `isGlobal` | body | `boolean` | no | Request body field. |
| `targetingGateID` | body | `string` | no | Request body field. |
| `monitoringMetrics` | body | `list` | no | Request body field. |
