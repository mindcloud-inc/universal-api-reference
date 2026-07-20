# Send Message to Conversation (SSE) with Stream with AssignX

Sends a message and returns streamed JSON SSE events.

## Endpoint

- **Method:** `POST`
- **Path:** `conversations/:id/jsonmessagesse`
- **Base URL:** `https://api.agentx.so/api/v1/access/`
- **Official documentation:** [Send Message to Conversation (SSE) with Stream](https://docs.agentx.so/reference/post_api-v1-access-conversations-id-jsonmessagesse)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Conversation identifier. |
| `message` | body | `string` | yes | Message text to send over JSON SSE. |
