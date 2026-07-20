# Retrieve Experiment Checks Diagnostics with Statsig

Retrieves experiment checks diagnostics from Statsig.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/experiments/{id}/diagnostics_checks`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Retrieve Experiment Checks Diagnostics](https://docs.statsig.com/api-reference/experiments/retrieve-experiment-checks-diagnostics)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `type` | query | `string` | no | — |
| `startDate` | query | `string` | no | Start date in YYYY-MM-DD format |
| `endDate` | query | `string` | no | End date in YYYY-MM-DD format |
