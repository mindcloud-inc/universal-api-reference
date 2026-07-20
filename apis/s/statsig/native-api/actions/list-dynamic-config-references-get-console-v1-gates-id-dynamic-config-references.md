# List Dynamic Config References with Statsig

Retrieves dynamic config references from Statsig.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/gates/{id}/dynamic_config_references`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [List Dynamic Config References](https://docs.statsig.com/api-reference/gates/list-dynamic-config-references)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `limit` | query | `number` | no | — |
| `page` | query | `number` | no | Page number |
