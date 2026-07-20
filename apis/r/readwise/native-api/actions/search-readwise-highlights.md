# Search Readwise Highlights with Readwise

Finds highlights in Readwise by semantic search.

## Endpoint

- **Method:** `POST`
- **Path:** `https://mcp2.readwise.io/mcp`
- **Base URL:** `https://readwise.io`
- **Official documentation:** [Search Readwise Highlights](https://github.com/readwiseio/readwise-cli)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json, text/event-stream` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params.arguments.vector_search_term` | body | `string` | yes | Searches highlight content using vector search. |
| `params.arguments.limit` | body | `number` | no | Maximum number of highlights to return. |
