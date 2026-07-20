# Update holdout by id with Statsig

Updates a holdout in Statsig by ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/holdouts/{id}`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Update holdout by id](https://docs.statsig.com/api-reference/holdouts/update-holdout-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `isEnabled` | body | `boolean` | yes | Request body field. |
| `description` | body | `string` | yes | Request body field. |
| `passPercentage` | body | `number` | yes | Request body field. |
| `gateIDs` | body | `list` | yes | Request body field. |
| `experimentIDs` | body | `list` | yes | Request body field. |
| `layerIDs` | body | `list` | yes | Request body field. |
| `isGlobal` | body | `boolean` | yes | Request body field. |
| `targetingGateID` | body | `string` | yes | Request body field. |
| `monitoringMetrics` | body | `list` | no | Request body field. |
