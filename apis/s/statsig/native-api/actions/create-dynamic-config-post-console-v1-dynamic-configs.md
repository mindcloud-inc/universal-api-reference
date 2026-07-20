# Create Dynamic Config with Statsig

Creates a dynamic config in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/dynamic_configs`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Create Dynamic Config](https://docs.statsig.com/api-reference/dynamic-configs/create-dynamic-config)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Request body field. |
| `isEnabled` | body | `boolean` | no | Request body field. |
| `description` | body | `string` | no | Request body field. |
| `rules` | body | `list` | no | Request body field. |
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
| `id` | body | `string` | no | Request body field. |
| `isTemplate` | body | `boolean` | no | Request body field. |
