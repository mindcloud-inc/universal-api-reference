# Create Thread Messages with Langbase

## Endpoint

- **Method:** `POST`
- **Path:** `v1/threads/:threadId/messages`
- **Base URL:** `https://api.langbase.com`
- **Official documentation:** [Create Thread Messages](https://langbase.com/docs/api-reference/threads/append-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `threadId` | path | `string` | yes | Thread ID that will receive the new messages. |
| `messages[]` | body | `array<object>` | yes | Array of thread message objects to append. |
