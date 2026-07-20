# Resolve Metric Rollout Alert with Statsig

Resolves a metric rollout alert in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/gates/{id}/alerts/{metricId}/resolve`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Resolve Metric Rollout Alert](https://docs.statsig.com/api-reference/gates/resolve-metric-rollout-alert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `metricId` | path | `string` | yes | metric id |
| `reasoning` | body | `string` | no | Request body field. |
