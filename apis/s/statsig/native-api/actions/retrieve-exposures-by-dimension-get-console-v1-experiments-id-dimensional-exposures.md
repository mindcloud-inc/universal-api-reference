# Retrieve Exposures By Dimension with Statsig

Retrieves exposures by dimension from Statsig.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/experiments/{id}/dimensional_exposures`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Retrieve Exposures By Dimension](https://docs.statsig.com/api-reference/experiments/retrieve-exposures-by-dimension)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `dimension_type` | query | `string` | no | Optional dimension type(s) to filter by (for example metadata.country). |
| `severity` | query | `string` | no | Optional severity filter: warning (p-value < 0.01) or failure (p-value < 0.001). |
