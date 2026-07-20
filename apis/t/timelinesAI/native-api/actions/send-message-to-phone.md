# Send Message to Phone with TimelinesAI

Creates a WhatsApp message in TimelinesAI by phone number.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages`
- **Base URL:** `https://app.timelines.ai/integrations/api`
- **Official documentation:** [Send Message to Phone](https://timelinesai.mintlify.app/public-api-reference/send-message-to-phone-number)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phone` | body | `string` | yes | Phone number in international format. |
| `whatsapp_account_phone` | body | `string` | no | Optional sending WhatsApp account phone number in international format. |
| `text` | body | `string` | no | Plain text message to send. |
| `file_uid` | body | `string` | no | Uploaded attachment UID to send with the message. |
| `label` | body | `string` | no | Label to assign to the chat while sending the message. |
| `attachment_template_id` | body | `number` | no | Attachment template ID to send with the message. |
