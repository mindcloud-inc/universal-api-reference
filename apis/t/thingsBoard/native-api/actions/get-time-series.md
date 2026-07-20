# Get Time Series with ThingsBoard

Retrieves latest time series values from ThingsBoard.

## Endpoint

- **Method:** `GET`
- **Path:** `/plugins/telemetry/:entityType/:entityId/values/timeseries`
- **Base URL:** `{baseUrl}/api`
- **Official documentation:** [Get Time Series](https://thingsboard.cloud/swagger-ui/index.html#/telemetry-controller/getLatestTimeseries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entityType` | path | `string` | yes | The ThingsBoard entity type, for example DEVICE. |
| `entityId` | path | `string` | yes | The ThingsBoard entity ID. |
| `params` | query | `string` | yes | Additional provider-specific telemetry query parameters. |
| `startTs` | query | `number` | yes | Start of the time range in Unix milliseconds. |
| `endTs` | query | `number` | yes | End of the time range in Unix milliseconds. |
