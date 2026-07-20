# Create Reader Document with Readwise

Creates a new document in Readwise Reader.

## Endpoint

- **Method:** `POST`
- **Path:** `https://mcp2.readwise.io/mcp`
- **Base URL:** `https://readwise.io`
- **Official documentation:** [Create Reader Document](https://github.com/readwiseio/readwise-cli)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json, text/event-stream` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params.arguments.url` | body | `string` | no | URL to save to Reader. |
| `params.arguments.html` | body | `string` | no | HTML content to create as a Reader document. |
| `params.arguments.markdown` | body | `string` | no | Markdown content to create as a Reader document. |
| `params.arguments.title` | body | `string` | no | Document title. |
