# List Vector Stores with Open AI

Retrieves vector stores from Open AI.

## Endpoint

- **Method:** `GET`
- **Path:** `v1/vector_stores`
- **Base URL:** `https://api.openai.com`
- **Official documentation:** [List Vector Stores](https://developers.openai.com/api/reference/vector-stores/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of vector stores to return. |
| `order` | query | `string` | no | Sort order by created time. |
