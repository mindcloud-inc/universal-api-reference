# List Pipelines with Statsig

Retrieves pipelines from Statsig.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/release_pipelines`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [List Pipelines](https://docs.statsig.com/api-reference/release-pipelines/list-pipelines)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Results per page |
| `page` | query | `number` | no | Page number |
