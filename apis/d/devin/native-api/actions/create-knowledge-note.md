# Create Knowledge Note with Devin

Creates a knowledge note in Devin.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/organizations/:org_id/knowledge/notes`
- **Base URL:** `https://api.devin.ai`
- **Official documentation:** [Create Knowledge Note](https://docs.devin.ai/api-reference/v3/notes/post-organizations-knowledge-notes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | yes | Knowledge note body. |
| `name` | body | `string` | yes | Knowledge note name. |
| `org_id` | path | `string` | yes | Devin organization ID. |
| `trigger` | body | `string` | yes | Knowledge note trigger text. |
