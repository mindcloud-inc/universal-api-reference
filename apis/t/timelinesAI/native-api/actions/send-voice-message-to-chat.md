# Send Voice Message To Chat with TimelinesAI

Creates a voice message in an existing TimelinesAI chat.

## Endpoint

- **Method:** `POST`
- **Path:** `/chats/{chat_id}/voice_message`
- **Base URL:** `https://app.timelines.ai/integrations/api`
- **Official documentation:** [Send Voice Message To Chat](https://timelinesai.mintlify.app/public-api-reference/post-chats-voice_message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chat_id` | path | `number` | yes | ID of the chat in TimelinesAI. You can find it in the chat URL or outbound webhook payload. |
| `file` | body | `file` | yes | Voice message audio file to upload and send. |
