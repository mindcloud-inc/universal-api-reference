# Build Extract Datamodel with Sisense

Starts an extract datamodel build in Sisense.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/builds`
- **Base URL:** `https://signup-126940n0.sisense.com`
- **Official documentation:** [Build Extract Datamodel](https://developer.sisense.com/guides/restApi/datamodels.v2.html#building-extract-datamodels)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datamodelId` | body | `string` | yes | Datamodel OID to build. |
| `buildType` | body | `string` | yes | Build type: full, by_table, or schema_changes. |
| `schemaOrigin` | body | `string` | no | Schema origin: latest or running. |
| `rowLimit` | body | `number` | no | Optional sample row limit. |
