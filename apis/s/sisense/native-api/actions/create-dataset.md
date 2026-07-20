# Create Dataset with Sisense

Creates a dataset in a Sisense datamodel.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/datamodels/:datamodelId/datasets`
- **Base URL:** `https://signup-126940n0.sisense.com`
- **Official documentation:** [Create Dataset](https://developer.sisense.com/guides/restApi/datamodels.v2.html#creating-a-dataset)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datamodelId` | path | `string` | yes | Datamodel OID. |
| `name` | body | `string` | yes | Dataset name. |
| `type` | body | `string` | no | Dataset type. Use custom for a connector-free dataset or extract for a connected dataset. |
| `connection.oid` | body | `string` | no | Connection OID for extract datasets. |
| `database` | body | `string` | no | Database name for extract datasets when required by the connector. |
| `schemaName` | body | `string` | no | Schema name for extract datasets when required by the connector. |
