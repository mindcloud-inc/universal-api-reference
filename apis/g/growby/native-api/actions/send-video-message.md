# Send Video Message with Growby

Sends a video message through Growby.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/messages`
- **Base URL:** `https://api.growby.net`
- **Official documentation:** [Send Video Message](https://www.postman.com/growby-documentation/growby-api/folder/l29qmmq/v3-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | yes | WhatsApp business phone number with country code. |
| `message.text` | body | `string` | no | Optional caption shown with the video. |
| `show_in_inbox` | body | `string` | no | Whether to show the message in the Growby inbox. |
| `to` | body | `string` | yes | Recipient phone number with country code. |
| `message.link` | body | `string` | yes | Publicly accessible MP4 or 3GP video URL. |
