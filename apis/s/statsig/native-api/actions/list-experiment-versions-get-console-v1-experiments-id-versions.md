# List Experiment Versions with Statsig

Retrieves experiment versions from Statsig.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/experiments/{id}/versions`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [List Experiment Versions](https://docs.statsig.com/api-reference/experiments/list-experiment-versions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `limit` | query | `number` | no | Results per page |
| `page` | query | `number` | no | Page number |
