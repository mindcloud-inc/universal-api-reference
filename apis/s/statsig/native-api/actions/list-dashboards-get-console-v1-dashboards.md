# List Dashboards with Statsig

Retrieves dashboards from Statsig.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/dashboards`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [List Dashboards](https://docs.statsig.com/api-reference/dashboards/list-dashboards)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Results per page |
| `page` | query | `number` | no | Page number |
| `search` | query | `string` | no | Filter dashboards by name using a partial match. |
