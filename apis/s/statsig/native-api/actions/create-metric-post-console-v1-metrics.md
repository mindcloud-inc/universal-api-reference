# Create Metric with Statsig

Creates a metric in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/metrics`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Create Metric](https://docs.statsig.com/api-reference/metrics/create-metric)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Request body field. |
| `type` | body | `string` | yes | Request body field. |
| `isVerified` | body | `boolean` | no | Request body field. |
| `isReadOnly` | body | `boolean` | no | Request body field. |
| `unitTypes` | body | `list` | no | Request body field. |
| `metricEvents` | body | `list` | no | Request body field. |
| `metricComponentMetrics` | body | `list` | no | Request body field. |
| `description` | body | `string` | no | Request body field. |
| `directionality` | body | `string` | no | Request body field. |
| `tags` | body | `string` | no | Request body field. |
| `isPermanent` | body | `boolean` | no | Request body field. |
| `rollupTimeWindow` | body | `string` | no | Request body field. |
| `customRollUpStart` | body | `number` | no | Request body field. |
| `customRollUpEnd` | body | `number` | no | Request body field. |
| `funnelEventList` | body | `list` | no | Request body field. |
| `funnelCountDistinct` | body | `string` | no | Request body field. |
| `warehouseNative` | body | `object` | no | Request body field. |
| `team` | body | `string` | no | Request body field. |
| `teamID` | body | `string` | no | Request body field. |
| `dryRun` | body | `boolean` | no | Request body field. |
