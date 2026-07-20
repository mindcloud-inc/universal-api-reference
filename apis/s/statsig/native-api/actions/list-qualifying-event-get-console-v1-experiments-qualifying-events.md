# List qualifying event with Statsig

Retrieves qualifying events from Statsig.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/experiments/qualifying_events`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [List qualifying event](https://docs.statsig.com/api-reference/experiments-warehouse-native/list-qualifying-event)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Results per page |
| `page` | query | `number` | no | Page number |
