# Move Reader Documents with Readwise

Updates document locations in Readwise Reader.

## Endpoint

- **Method:** `POST`
- **Path:** `https://mcp2.readwise.io/mcp`
- **Base URL:** `https://readwise.io`
- **Official documentation:** [Move Reader Documents](https://github.com/readwiseio/readwise-cli)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json, text/event-stream` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params.arguments.document_ids` | body | `string` | yes | Comma-separated Reader document IDs to move. |
| `params.arguments.location` | body | `string` | yes | Destination location: new, later, shortlist, archive, or feed. |
