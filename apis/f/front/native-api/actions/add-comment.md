# Add Comment with Front

Creates a conversation comment in Front.

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations/:conversation_id/comments`
- **Base URL:** `https://api2.frontapp.com`
- **Official documentation:** [Add Comment](https://dev.frontapp.com/reference/add-comment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | The conversation ID. |
| `body` | body | `string` | yes | Content of the comment. Can include markdown formatting. |
| `author_id` | body | `string` | no | ID of the teammate creating the comment. |
| `is_pinned` | body | `boolean` | no | Whether the comment is pinned in its conversation. |
