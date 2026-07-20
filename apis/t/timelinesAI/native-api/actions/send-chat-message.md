# Send Chat Message with TimelinesAI

Creates a new message in an existing TimelinesAI chat.

## Endpoint

- **Method:** `POST`
- **Path:** `/chats/{chat_id}/messages`
- **Base URL:** `https://app.timelines.ai/integrations/api`
- **Official documentation:** [Send Chat Message](https://timelinesai.mintlify.app/public-api-reference/send-message-in-existing-chat)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chat_id` | path | `number` | yes | ID of the chat in TimelinesAI. You can find it in the chat URL or outbound webhook payload. |
| `text` | body | `string` | no | Plain text message to send. |
| `file_uid` | body | `string` | no | Uploaded attachment UID to send with the message. |
| `label` | body | `string` | no | Label to assign to the chat while sending the message. |
| `attachment_template_id` | body | `number` | no | Attachment template ID to send with the message. |
| `reply_to` | body | `string` | no | Message UID to reply to. |
