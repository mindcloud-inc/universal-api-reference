# Get Sandbox Metrics with Daytona

Retrieves sandbox metrics from Daytona.

## Endpoint

- **Method:** `GET`
- **Path:** `/sandbox/[:sandboxId]/telemetry/metrics`
- **Base URL:** `https://app.daytona.io/api`
- **Official documentation:** [Get Sandbox Metrics](https://www.daytona.io/docs/tools/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sandboxId` | path | `string` | yes | ID of the sandbox. |
| `from` | query | `date` | yes | Start of time range (ISO 8601). |
| `to` | query | `date` | yes | End of time range (ISO 8601). |
| `metricNames[]` | query | `array<string>` | no | Filter by metric names. |
