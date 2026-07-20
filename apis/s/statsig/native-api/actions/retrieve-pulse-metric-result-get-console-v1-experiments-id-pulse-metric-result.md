# Retrieve Pulse Metric Result with Statsig

Retrieves a pulse metric result from Statsig.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/experiments/{id}/pulse_metric_result`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Retrieve Pulse Metric Result](https://docs.statsig.com/api-reference/experiments/retrieve-pulse-metric-result)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `control` | query | `string` | yes | Control Group ID |
| `test` | query | `string` | yes | Test Group ID |
| `cuped` | query | `string` | no | Whether to apply CUPED. Allowed values are "true" or "false". |
| `confidence` | query | `string` | no | Confidence interval (0-100) |
| `applyBonferroniPerVariant` | query | `string` | no | Whether to apply Bonferroni Per Variant. Allowed values are "true" or "false". |
| `applyBonferroniPerMetric` | query | `string` | no | Whether to apply Bonferroni Per Metric. Allowed values are "true" or "false". |
| `bonferroniPrimaryMetricWeight` | query | `string` | no | α allocated to primary metrics |
| `applyBenjaminiHochbergPerMetric` | query | `string` | no | Whether to apply Benjamini-Hochberg Correction Per Metric. Allowed values are "true" or "false". |
| `applyBenjaminiHochbergPerVariant` | query | `string` | no | Whether to apply Benjamini-Hochberg Correction Per Variant. Allowed values are "true" or "false". |
| `date` | query | `string` | no | Date for pulse results. format must be YYYY-MM-DD |
| `metricID` | query | `string` | yes | Metric ID in format <metric_name>::<metric_type> |
