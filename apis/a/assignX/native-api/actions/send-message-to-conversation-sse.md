# Send Message to Conversation (SSE) with AssignX

Sends a message and returns SSE events in AssignX.

## Endpoint

- **Method:** `POST`
- **Path:** `conversations/:id/messagesse`
- **Base URL:** `https://api.agentx.so/api/v1/access/`
- **Official documentation:** [Send Message to Conversation (SSE)](https://docs.agentx.so/reference/post_api-v1-access-conversations-id-messagesse-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Conversation identifier. |
| `message` | body | `string` | yes | Message text to send over SSE. |
