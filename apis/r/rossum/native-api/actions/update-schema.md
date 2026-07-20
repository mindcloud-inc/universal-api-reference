# Update Schema with Rossum

Updates a schema in Rossum.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/schemas/:schemaID`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [Update Schema](https://rossum.app/api/docs/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Updated schema name. |
| `schemaID` | path | `number` | yes | Rossum schema ID. |
