# Add Chat Labels with TimelinesAI

Adds labels to a specific TimelinesAI chat.

## Endpoint

- **Method:** `PUT`
- **Path:** `/chats/{chat_id}/labels`
- **Base URL:** `https://app.timelines.ai/integrations/api`
- **Official documentation:** [Add Chat Labels](https://timelinesai.mintlify.app/public-api-reference/adds-labels-for-the-chat)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chat_id` | path | `number` | yes | ID of the chat in TimelinesAI. You can find it in the chat URL or outbound webhook payload. |
| `labels[]` | body | `array<string>` | yes | Labels to add to the chat. |
