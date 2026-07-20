# Get Chat with TimelinesAI

Retrieves details for a TimelinesAI chat.

## Endpoint

- **Method:** `GET`
- **Path:** `/chats/{chat_id}`
- **Base URL:** `https://app.timelines.ai/integrations/api`
- **Official documentation:** [Get Chat](https://timelinesai.mintlify.app/public-api-reference/get-details-of-a-chat)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chat_id` | path | `number` | yes | ID of the chat in TimelinesAI. You can find it in the chat URL or outbound webhook payload. |
