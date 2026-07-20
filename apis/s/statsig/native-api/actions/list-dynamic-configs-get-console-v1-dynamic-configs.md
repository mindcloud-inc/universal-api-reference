# List Dynamic Configs with Statsig

Retrieves dynamic configs from Statsig.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/dynamic_configs`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [List Dynamic Configs](https://docs.statsig.com/api-reference/dynamic-configs/list-dynamic-configs)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `releasePipelineID` | query | `string` | no | The release pipeline ID associated with the dynamic config |
| `teamID` | query | `string` | no | Filter by team ID |
| `targetAppID` | query | `string` | no | Filter by target app ID |
| `creatorName` | query | `string` | no | Name of the creator. |
| `creatorID` | query | `string` | no | ID of the user who created the entity. |
| `tags` | query | `string` | no | Filter by tags |
| `limit` | query | `number` | no | Results per page |
| `page` | query | `number` | no | Page number |
