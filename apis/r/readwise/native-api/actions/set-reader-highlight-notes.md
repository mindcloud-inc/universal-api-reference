# Set Reader Highlight Notes with Readwise

Updates notes on a Readwise Reader highlight.

## Endpoint

- **Method:** `POST`
- **Path:** `https://mcp2.readwise.io/mcp`
- **Base URL:** `https://readwise.io`
- **Official documentation:** [Set Reader Highlight Notes](https://github.com/readwiseio/readwise-cli)

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
| `params.arguments.notes` | body | `string` | no | Notes to set for the highlight. Empty clears notes. |
