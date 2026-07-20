# Send Message V2 with Growby

Sends a message through Growby v2.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/messages`
- **Base URL:** `https://api.growby.net`
- **Official documentation:** [Send Message V2](https://www.postman.com/growby-documentation/growby-api/folder/u5nohd1/send-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | no | WhatsApp sender number with country code. |
| `text` | body | `string` | no | Text message body for the v2 endpoint. |
| `to` | body | `string` | no | Recipient phone number with country code. |
| `type` | body | `string` | no | Older v2 message type, for example text. |
