# Search Reader Documents with Readwise

Finds documents in Readwise Reader by query.

## Endpoint

- **Method:** `POST`
- **Path:** `https://mcp2.readwise.io/mcp`
- **Base URL:** `https://readwise.io`
- **Official documentation:** [Search Reader Documents](https://github.com/readwiseio/readwise-cli)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json, text/event-stream` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params.arguments.query` | body | `string` | yes | Search query for Reader documents. |
| `params.arguments.limit` | body | `number` | no | Maximum number of documents to return. |
