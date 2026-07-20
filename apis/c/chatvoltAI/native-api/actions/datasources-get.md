# Get Datasource with Chatvolt AI

Retrieves a datasource from Chatvolt AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/datasources/{id}`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Get Datasource](https://docs.chatvolt.ai/api-reference/endpoint/datasources/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the data source to be retrieved. |
| `idstore` | query | `string` | yes | ID of the datastore to which the datasource belongs (used for validation). |
