# Get specific events with Statsig

Retrieves a specific event from Statsig.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/events/{eventName}`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Get specific events](https://docs.statsig.com/api-reference/events/get-specific-events)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventName` | path | `string` | yes | — |
| `limit` | query | `number` | no | Results per page |
| `page` | query | `number` | no | Page number |
