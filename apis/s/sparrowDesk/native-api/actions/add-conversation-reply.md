# Add Conversation Reply with SparrowDesk

Creates a conversation reply in SparrowDesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations/{{id}}/reply`
- **Base URL:** `https://api.sparrowdesk.com/v1`
- **Official documentation:** [Add Conversation Reply](https://developer.sparrowdesk.com/rest-api/endpoints/conversations/id/reply/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | SparrowDesk conversation ID. |
| `reply_text` | body | `string` | yes | Reply or internal note content. |
| `type` | body | `string` | yes | REPLY or INTERNAL_NOTE. |
