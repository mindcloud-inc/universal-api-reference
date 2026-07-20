# List Chat Labels with TimelinesAI

Retrieves labels for a specific TimelinesAI chat.

## Endpoint

- **Method:** `GET`
- **Path:** `/chats/{chat_id}/labels`
- **Base URL:** `https://app.timelines.ai/integrations/api`
- **Official documentation:** [List Chat Labels](https://timelinesai.mintlify.app/public-api-reference/list-labels-for-the-specified-chat)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chat_id` | path | `number` | yes | ID of the chat in TimelinesAI. You can find it in the chat URL or outbound webhook payload. |
