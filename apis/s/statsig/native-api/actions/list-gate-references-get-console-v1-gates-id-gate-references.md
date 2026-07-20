# List Gate References with Statsig

Retrieves gate references from Statsig.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/gates/{id}/gate_references`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [List Gate References](https://docs.statsig.com/api-reference/gates/list-gate-references)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `limit` | query | `number` | no | — |
| `page` | query | `number` | no | Page number |
