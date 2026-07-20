# Send Message to JID with TimelinesAI

Creates a WhatsApp message in TimelinesAI by JID.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages/to_jid`
- **Base URL:** `https://app.timelines.ai/integrations/api`
- **Official documentation:** [Send Message to JID](https://timelinesai.mintlify.app/public-api-reference/send-message-to-jid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jid` | body | `string` | yes | WhatsApp JID of the contact or group. |
| `whatsapp_account_phone` | body | `string` | no | Optional sending WhatsApp account phone number in international format. |
| `reply_to` | body | `string` | no | Message UID to reply to. |
| `text` | body | `string` | no | Plain text message to send. |
| `file_uid` | body | `string` | no | Uploaded attachment UID to send with the message. |
| `label` | body | `string` | no | Label to assign to the chat while sending the message. |
| `attachment_template_id` | body | `number` | no | Attachment template ID to send with the message. |
