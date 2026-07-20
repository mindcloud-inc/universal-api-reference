# Get Reports with Statsig

Retrieves reports from Statsig.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/reports`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Get Reports](https://docs.statsig.com/api-reference/reports/get-reports)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `string` | yes | report type |
| `date` | query | `string` | yes | date for the report |
