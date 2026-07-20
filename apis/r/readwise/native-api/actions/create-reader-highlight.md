# Create Reader Highlight with Readwise

Creates a new highlight in Readwise Reader.

## Endpoint

- **Method:** `POST`
- **Path:** `https://mcp2.readwise.io/mcp`
- **Base URL:** `https://readwise.io`
- **Official documentation:** [Create Reader Highlight](https://github.com/readwiseio/readwise-cli)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json, text/event-stream` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params.arguments.document_id` | body | `string` | yes | Reader document ID to highlight. |
| `params.arguments.html_content` | body | `string` | yes | Exact HTML fragment to highlight. |
| `params.arguments.tags` | body | `string` | no | Optional tag names to apply. |
| `params.arguments.note` | body | `string` | no | Optional note to attach. |
