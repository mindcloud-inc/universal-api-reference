# List Dynamic Config Versions with Statsig

Retrieves dynamic config versions from Statsig.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/dynamic_configs/{id}/versions`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [List Dynamic Config Versions](https://docs.statsig.com/api-reference/dynamic-configs/list-dynamic-config-versions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `limit` | query | `number` | no | Results per page |
| `page` | query | `number` | no | Page number |
