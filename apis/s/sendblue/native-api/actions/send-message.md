# Send Message with Sendblue

Sends a message through Sendblue.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/send-message`
- **Base URL:** `https://api.sendblue.co`
- **Official documentation:** [Send Message](https://docs.sendblue.com/api/resources/messages/methods/send/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `number` | body | `string` | yes | Recipient phone number in E.164 format. |
| `content` | body | `string` | yes | Message content. |
| `from_number` | body | `string` | yes | Sendblue number to send from. |
| `send_style` | body | `string` | no | Send style. Docs list default, invisible, and '8ball'. |
| `media_url` | body | `string` | no | Remote media URL to attach. |
