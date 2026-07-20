# Send Message To Chat Name with TimelinesAI

Creates a WhatsApp message in TimelinesAI by chat name.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages/to_chat_name`
- **Base URL:** `https://app.timelines.ai/integrations/api`
- **Official documentation:** [Send Message To Chat Name](https://timelinesai.mintlify.app/public-api-reference/send-message-in-existing-chat-specified-by-chat-name)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chat_name` | body | `string` | yes | Exact chat name as it appears in TimelinesAI. |
| `reply_to` | body | `string` | no | Message UID to reply to. |
| `text` | body | `string` | no | Plain text message to send. |
| `file_uid` | body | `string` | no | Uploaded attachment UID to send with the message. |
| `label` | body | `string` | no | Label to assign to the chat while sending the message. |
| `attachment_template_id` | body | `number` | no | Attachment template ID to send with the message. |
