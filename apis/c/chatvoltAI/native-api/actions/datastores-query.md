# Query Datastore with Chatvolt AI

Queries a datastore in Chatvolt AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/datastores/{id}/query`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Query Datastore](https://docs.chatvolt.ai/api-reference/endpoint/datastores/query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the datastore |
| `query` | body | `string` | yes | Query to ask your Datastore. |
| `topK` | body | `number` | no | The maximum number of results to retrieve. |
| `filters` | body | `object` | no | Filters for application/json requests. |
