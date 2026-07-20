# Remove Tags From Reader Highlight with Readwise

Removes tags from a highlight in Readwise Reader.

## Endpoint

- **Method:** `POST`
- **Path:** `https://mcp2.readwise.io/mcp`
- **Base URL:** `https://readwise.io`
- **Official documentation:** [Remove Tags From Reader Highlight](https://github.com/readwiseio/readwise-cli)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json, text/event-stream` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params.arguments.document_id` | body | `string` | yes | Reader document ID containing the highlight. |
| `params.arguments.highlight_document_id` | body | `string` | yes | Reader highlight document ID. |
| `params.arguments.tag_names` | body | `string` | yes | Tag names to remove. |
