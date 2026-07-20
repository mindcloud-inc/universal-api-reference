# Update Readwise Highlight With Tags with Readwise

Updates a Readwise highlight and its tags.

## Endpoint

- **Method:** `POST`
- **Path:** `https://mcp2.readwise.io/mcp`
- **Base URL:** `https://readwise.io`
- **Official documentation:** [Update Readwise Highlight With Tags](https://github.com/readwiseio/readwise-cli)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json, text/event-stream` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params.arguments.highlight_id` | body | `string` | yes | Readwise highlight ID to update. |
| `params.arguments.text` | body | `string` | no | New highlight text. |
| `params.arguments.note` | body | `string` | no | New highlight note. |
| `params.arguments.add_tags` | body | `string` | no | Tag names to add. |
| `params.arguments.remove_tags` | body | `string` | no | Tag names to remove. |
