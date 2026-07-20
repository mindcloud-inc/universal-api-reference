# Query Document with AgentQL

Queries structured data from documents and images with AgentQL.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/query-document`
- **Base URL:** `https://api.agentql.com`
- **Official documentation:** [Query Document](https://docs.agentql.com/rest-api/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | — |
| `body` | body | `string` | yes | Stringified JSON containing query or prompt plus optional params. |
