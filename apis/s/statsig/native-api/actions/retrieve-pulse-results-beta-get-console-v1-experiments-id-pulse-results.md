# Retrieve Pulse Results (Beta) with Statsig

Retrieves pulse results from Statsig.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/experiments/{id}/pulse_results`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Retrieve Pulse Results (Beta)](https://docs.statsig.com/api-reference/experiments/retrieve-pulse-results-beta)

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
