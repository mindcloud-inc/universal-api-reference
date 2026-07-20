# Send Document Message with Growby

Sends a document message through Growby.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/messages`
- **Base URL:** `https://api.growby.net`
- **Official documentation:** [Send Document Message](https://www.postman.com/growby-documentation/growby-api/folder/l29qmmq/v3-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | yes | WhatsApp business phone number with country code. |
| `message.text` | body | `string` | no | Optional caption shown with the document. |
| `to` | body | `string` | yes | Recipient phone number with country code. |
| `message.link` | body | `string` | yes | Publicly accessible PDF URL. |
| `message.filename` | body | `string` | no | Optional filename for the document. |
| `show_in_inbox` | body | `boolean` | no | Whether to show the message in the Growby inbox. |
