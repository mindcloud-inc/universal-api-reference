# Read Exposure Event Count with Statsig

Retrieves exposure event counts from Statsig.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/exposure_count`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Read Exposure Event Count](https://docs.statsig.com/api-reference/configs/read-exposure-event-count)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `experiments` | query | `string` | no |
| `gates` | query | `string` | no |
| `dynamicConfigs` | query | `string` | no |
