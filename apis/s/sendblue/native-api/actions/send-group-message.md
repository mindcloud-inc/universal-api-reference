# Send Group Message with Sendblue

Sends a group message through Sendblue.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/send-group-message`
- **Base URL:** `https://api.sendblue.co`
- **Official documentation:** [Send Group Message](https://docs.sendblue.com/api/resources/groups/methods/send_message/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | no | Message text content. |
| `from_number` | body | `string` | yes | The Sendblue phone number to send from in E.164 format. |
| `group_id` | body | `string` | no | The identifier for an existing group. |
| `media_url` | body | `string` | no | A media file URL to send with the message. |
| `numbers[]` | body | `array<string>` | no | Recipient phone numbers in E.164 format. Send multiple values as a array. |
