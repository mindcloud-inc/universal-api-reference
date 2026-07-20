# Send Text Message with Growby

Sends a text message through Growby.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/messages`
- **Base URL:** `https://api.growby.net`
- **Official documentation:** [Send Text Message](https://www.postman.com/growby-documentation/growby-api/request/84rvkmu/send-text-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | yes | WhatsApp business phone number with country code, for example 15551234567 or +15551234567. |
| `to` | body | `string` | yes | Recipient phone number with country code, for example 15551234567 or +15551234567. |
| `message.text` | body | `string` | yes | Text content to send. Growby documents a maximum length of 4096 characters. |
| `show_in_inbox` | body | `boolean` | no | Whether to show the message in the Growby inbox. |
