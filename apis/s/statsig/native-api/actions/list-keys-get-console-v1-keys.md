# List Keys with Statsig

Retrieves keys from Statsig.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/keys`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [List Keys](https://docs.statsig.com/api-reference/keys/list-keys)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `primaryTargetApp` | query | `string` | no | — |
| `environment` | query | `string` | no | — |
| `limit` | query | `number` | no | Results per page |
| `page` | query | `number` | no | Page number |
