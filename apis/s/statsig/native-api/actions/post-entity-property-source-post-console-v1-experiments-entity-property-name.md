# Post Entity Property Source with Statsig

Creates an entity property source in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/experiments/entity_property/{name}`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Post Entity Property Source](https://docs.statsig.com/api-reference/experiments/post-entity-property-source)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | name |
| `description` | body | `string` | no | Request body field. |
| `tags` | body | `list` | no | Request body field. |
| `sql` | body | `string` | yes | Request body field. |
| `timestampColumn` | body | `string` | no | Request body field. |
| `timestampAsDay` | body | `boolean` | no | Request body field. |
| `idTypeMapping` | body | `list` | yes | Request body field. |
| `isReadOnly` | body | `boolean` | no | Request body field. |
| `team` | body | `string` | no | Request body field. |
| `teamID` | body | `string` | no | Request body field. |
| `dryRun` | body | `boolean` | no | Request body field. |
