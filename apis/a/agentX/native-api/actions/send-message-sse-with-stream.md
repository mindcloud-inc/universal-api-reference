# Send Message SSE With Stream with AgentX

Sends a conversation message with SSE streaming in AgentX.

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations/:id/jsonmessagesse`
- **Base URL:** `https://api.agentx.so/api/v1/access`
- **Official documentation:** [Send Message SSE With Stream](https://docs.agentx.so/reference/post_api-v1-access-conversations-id-jsonmessagesse)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Conversation Id |
| `message` | body | `string` | yes | Message to send |
| `context` | body | `number` | no | Context for the message |
| `audio` | body | `object` | no | Audio metadata object with base64, duration, and optional url |
| `attachments[]` | body | `array<object>` | no | Attachment array with url, mimetype, filename, originalname, size, and createdAt |
