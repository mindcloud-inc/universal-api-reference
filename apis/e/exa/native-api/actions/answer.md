# Answer with Exa

Retrieves an answer from Exa.

## Endpoint

- **Method:** `POST`
- **Path:** `/answer`
- **Base URL:** `https://api.exa.ai`
- **Official documentation:** [Answer](https://exa.ai/docs/reference/answer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | The question or query to answer. |
| `stream` | body | `boolean` | no | If true, the response is returned as a server-sent events (SSS) stream. |
| `text` | body | `boolean` | no | If true, the response includes full text content in the search results |
