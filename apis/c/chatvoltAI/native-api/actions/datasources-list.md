# List Datasources with Chatvolt AI

Retrieves datasources from Chatvolt AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/datasources/list`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [List Datasources](https://docs.chatvolt.ai/api-reference/endpoint/datasources/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datastoreId` | query | `string` | yes | ID of the datastore to list datasources from. |
| `offset` | query | `number` | no | Number of items to skip. |
| `limit` | query | `number` | no | Maximum number of items to return. |
