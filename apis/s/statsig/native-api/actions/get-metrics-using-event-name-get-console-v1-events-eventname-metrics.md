# Get metrics using event name with Statsig

Retrieves metrics from Statsig by event name.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/events/{eventName}/metrics`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Get metrics using event name](https://docs.statsig.com/api-reference/events/get-metrics-using-event-name)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventName` | path | `string` | yes | — |
| `limit` | query | `number` | no | Results per page |
| `page` | query | `number` | no | Page number |
