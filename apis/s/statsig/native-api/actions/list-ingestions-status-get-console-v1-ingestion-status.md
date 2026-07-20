# List Ingestions Status with Statsig

Retrieves ingestion statuses from Statsig.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/ingestion/status`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [List Ingestions Status](https://docs.statsig.com/api-reference/ingestions/list-ingestions-status)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startDate` | query | `string` | yes | Expected valid date in the form of YYYY-MM-DD |
| `endDate` | query | `string` | yes | Expected valid date in the form of YYYY-MM-DD |
| `source` | query | `string` | no | — |
| `dataset` | query | `string` | no | — |
| `status` | query | `string` | no | — |
| `statuses` | query | `list` | no | — |
