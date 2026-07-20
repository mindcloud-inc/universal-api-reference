# Partially Update Autotune with Statsig

Updates an autotune in Statsig.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/console/v1/autotunes/{id}`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Partially Update Autotune](https://docs.statsig.com/api-reference/autotunes/partially-update-autotune)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `description` | body | `string` | no | Request body field. |
| `variants` | body | `list` | no | Request body field. |
| `successEvent` | body | `string` | no | Request body field. |
| `successEventValue` | body | `string` | no | Request body field. |
| `explorationWindow` | body | `string` | no | Request body field. |
| `attributionWindow` | body | `string` | no | Request body field. |
| `attributionWindowUnit` | body | `string` | no | Request body field. |
| `explorationWindowRate` | body | `number` | no | Request body field. |
| `longtermExplorationAllocation` | body | `number` | no | Request body field. |
| `winnerThreshold` | body | `string` | no | Request body field. |
| `metadataField` | body | `string` | no | Request body field. |
| `higherIsBetter` | body | `boolean` | no | Request body field. |
| `isContextual` | body | `boolean` | no | Request body field. |
| `metricSourceID` | body | `string` | no | Request body field. |
| `linkedExperimentName` | body | `string` | no | Request body field. |
| `goalRichText` | body | `string` | no | Request body field. |
| `optimizationParameter` | body | `string` | no | Request body field. |
| `valueColumn` | body | `string` | no | Request body field. |
| `featureList` | body | `list` | no | Request body field. |
