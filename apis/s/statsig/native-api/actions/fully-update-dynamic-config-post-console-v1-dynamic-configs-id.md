# Fully Update Dynamic Config with Statsig

Updates a dynamic config in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/dynamic_configs/{id}`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Fully Update Dynamic Config](https://docs.statsig.com/api-reference/dynamic-configs/fully-update-dynamic-config)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `dryRun` | query | `boolean` | no | Skips persisting updates to the entity (used to validate that inputs are correct) |
| `name` | body | `string` | no | Request body field. |
| `isEnabled` | body | `boolean` | yes | Request body field. |
| `description` | body | `string` | yes | Request body field. |
| `rules` | body | `list` | yes | Request body field. |
| `defaultValue` | body | `object` | no | Request body field. |
| `defaultValueJson5` | body | `string` | no | Request body field. |
| `idType` | body | `string` | no | Request body field. |
| `tags` | body | `list` | no | Request body field. |
| `creatorID` | body | `string` | no | Request body field. |
| `owner` | body | `object` | no | Request body field. |
| `creatorEmail` | body | `string` | no | Request body field. |
| `schema` | body | `string` | no | Request body field. |
| `schemaJson5` | body | `string` | no | Request body field. |
| `targetApps` | body | `string` | no | Request body field. |
| `team` | body | `string` | no | Request body field. |
| `teamID` | body | `string` | no | Request body field. |
| `releasePipelineID` | body | `string` | no | Request body field. |
