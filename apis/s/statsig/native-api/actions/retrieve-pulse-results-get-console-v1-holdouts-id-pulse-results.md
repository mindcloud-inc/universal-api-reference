# Retrieve Pulse Results with Statsig

Retrieves pulse results from Statsig.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/holdouts/{id}/pulse_results`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Retrieve Pulse Results](https://docs.statsig.com/api-reference/holdouts/retrieve-pulse-results)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `cuped` | query | `string` | no | Whether to apply CUPED. Allowed values are "true" or "false". |
| `confidence` | query | `string` | no | Confidence interval (0-100) |
