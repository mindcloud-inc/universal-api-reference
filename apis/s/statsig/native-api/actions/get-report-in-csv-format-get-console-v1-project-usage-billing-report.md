# Get Report in CSV format with Statsig

Retrieves a report from Statsig in CSV format.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/project/usage_billing/report`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Get Report in CSV format](https://docs.statsig.com/api-reference/usage/get-report-in-csv-format)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start` | query | `number` | no | Unix timestamp in ms |
| `end` | query | `number` | yes | Unix timestamp in ms |
