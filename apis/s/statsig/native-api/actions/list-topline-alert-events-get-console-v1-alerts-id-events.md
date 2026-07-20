# List Topline Alert Events with Statsig

Retrieves topline alert events from Statsig.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/alerts/{id}/events`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [List Topline Alert Events](https://docs.statsig.com/api-reference/alerts/list-topline-alert-events)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `limit` | query | `number` | no | Results per page |
| `page` | query | `number` | no | Page number |
