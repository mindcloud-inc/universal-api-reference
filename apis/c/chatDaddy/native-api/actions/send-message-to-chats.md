# Send Message to Chats with ChatDaddy

Sends a message to one or more ChatDaddy chats.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages`
- **Base URL:** `https://api.chatdaddy.tech/im`
- **Official documentation:** [Send Message to Chats](https://chatdaddy.stoplight.io/docs/openapi/26d693d66f6eb-send-a-message-to-one-or-more-chats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | query | `string` | yes | Account identifier to send from. |
| `compose` | body | `object` | no | Message composition payload, including text or attachments. |
| `recipients[]` | body | `array<object>` | yes | Recipient list for the bulk message send. |
