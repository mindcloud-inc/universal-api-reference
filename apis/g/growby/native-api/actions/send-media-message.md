# Send Media Message with Growby

Sends a media message through Growby.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/messages`
- **Base URL:** `https://api.growby.net`
- **Official documentation:** [Send Media Message](https://www.postman.com/growby-documentation/growby-api/request/mugkxwl/send-media-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | yes | WhatsApp business phone number with country code, for example 15551234567 or +15551234567. |
| `to` | body | `string` | yes | Recipient phone number with country code, for example 15551234567 or +15551234567. |
| `message.link` | body | `string` | yes | Publicly accessible image URL. Growby supports JPEG and PNG images up to 5 MB. |
| `message.text` | body | `string` | no | Optional caption shown with the media. |
| `show_in_inbox` | body | `boolean` | no | Whether to show the message in the Growby inbox. |
