# List Gate Versions with Statsig

Retrieves gate versions from Statsig.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/gates/{id}/versions`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [List Gate Versions](https://docs.statsig.com/api-reference/gates/list-gate-versions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `limit` | query | `number` | no | Results per page |
| `page` | query | `number` | no | Page number |
