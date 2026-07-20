# Create Autotune with Statsig

Creates an autotune in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/autotunes`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Create Autotune](https://docs.statsig.com/api-reference/autotunes/create-autotune)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Request body field. |
| `variants` | body | `list` | yes | Request body field. |
| `successEvent` | body | `string` | yes | Request body field. |
| `successEventValue` | body | `string` | no | Request body field. |
| `explorationWindow` | body | `string` | yes | Request body field. |
| `attributionWindow` | body | `string` | yes | Request body field. |
| `attributionWindowUnit` | body | `string` | no | Request body field. |
| `explorationWindowRate` | body | `number` | no | Request body field. |
| `longtermExplorationAllocation` | body | `number` | no | Request body field. |
| `winnerThreshold` | body | `string` | yes | Request body field. |
| `metadataField` | body | `string` | no | Request body field. |
| `higherIsBetter` | body | `boolean` | no | Request body field. |
| `isContextual` | body | `boolean` | no | Request body field. |
| `metricSourceID` | body | `string` | no | Request body field. |
| `linkedExperimentName` | body | `string` | no | Request body field. |
| `goalRichText` | body | `string` | no | Request body field. |
| `optimizationParameter` | body | `string` | no | Request body field. |
| `valueColumn` | body | `string` | no | Request body field. |
| `featureList` | body | `list` | no | Request body field. |
| `name` | body | `string` | yes | Request body field. |
| `idType` | body | `string` | no | Request body field. |
