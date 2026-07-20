# Send Message with Kommunicate

Creates a message in Kommunicate.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/ws/message/v2/send`
- **Base URL:** `https://services.kommunicate.io`
- **Official documentation:** [Send Message](https://docs.kommunicate.io/docs/api-detail#send-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | body | `string` | yes | Conversation identifier to send the message into. |
| `clientGroupId` | body | `string` | no | Optional client conversation identifier. |
| `message` | body | `string` | yes | Message text to send. |
| `fromUserName` | body | `string` | yes | Sender user ID. |
| `metadata` | body | `object` | no | Optional rich-message metadata. |
