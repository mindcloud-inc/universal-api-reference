# Get Datastore with Chatvolt AI

Retrieves a datastore from Chatvolt AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/datastores/{id}`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Get Datastore](https://docs.chatvolt.ai/api-reference/endpoint/datastores/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the datastore to be retrieved. |
| `search` | query | `string` | no | Term to search for datasources by name (case-insensitive). Optional. |
| `status` | query | `string` | no | Filters datasources by status. Optional. |
| `type` | query | `string` | no | Filters datasources by type. Optional. |
| `offset` | query | `number` | no | Number of pages to skip for datasource pagination. Optional. |
| `limit` | query | `number` | no | Maximum number of datasources to return per page. Optional. |
| `groupId` | query | `string` | no | Filtra datasources por um ID de grupo específico. Opcional. |
