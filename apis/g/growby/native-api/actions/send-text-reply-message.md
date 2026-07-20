# Send Text Reply Message with Growby

Sends a text reply message through Growby.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/reply-messages`
- **Base URL:** `https://api.growby.net`
- **Official documentation:** [Send Text Reply Message](https://www.postman.com/growby/workspace/growby/folder/29609016-3a876c37-d822-48be-b589-871f5fc2d7d6)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | no | Approved WhatsApp sender number. |
| `message_id` | body | `string` | no | Incoming WhatsApp message ID you are replying to. |
| `password` | body | `string` | no | Growby password for the v1 reply API. |
| `text` | body | `string` | no | Reply message text. |
| `to` | body | `string` | no | Recipient phone number with country code. |
| `type` | body | `string` | no | This action sends a text reply message. |
| `username` | body | `string` | no | Growby username for the v1 reply API. |
