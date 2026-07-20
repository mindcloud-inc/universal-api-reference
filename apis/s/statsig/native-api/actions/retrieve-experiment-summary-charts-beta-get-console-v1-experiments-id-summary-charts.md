# Retrieve Experiment Summary Charts (Beta) with Statsig

Retrieves experiment summary charts from Statsig.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/experiments/{id}/summary_charts`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Retrieve Experiment Summary Charts (Beta)](https://docs.statsig.com/api-reference/experiments/retrieve-experiment-summary-charts-beta)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `control` | query | `string` | no | Optional override control group ID |
| `test` | query | `string` | no | Optional override test group ID. Use "*" to query against all test groups. |
