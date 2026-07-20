# Update Dataset Connection with Sisense

Updates a dataset connection in Sisense.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/datamodels/:datamodelId/datasets/:datasetId`
- **Base URL:** `https://signup-126940n0.sisense.com`
- **Official documentation:** [Update Dataset Connection](https://developer.sisense.com/guides/restApi/datamodels.v2.html#changing-a-dataset-s-connection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `connection.oid` | body | `string` | no | The oid of the desired Sisense connection. |
| `datamodelId` | path | `string` | no | The Datamodel oid. |
| `datasetId` | path | `string` | no | The Dataset oid. |
