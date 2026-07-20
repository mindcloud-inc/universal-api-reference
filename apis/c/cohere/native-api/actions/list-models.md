# List Models with Cohere

Lists available AI models in Cohere.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/models`
- **Base URL:** `https://api.cohere.com`
- **Official documentation:** [List Models](https://docs.cohere.com/reference/list-models)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page_size` | query | `number` | no | Maximum number of models to return. |
| `page_token` | query | `string` | no | Opaque pagination token returned by Cohere. |
