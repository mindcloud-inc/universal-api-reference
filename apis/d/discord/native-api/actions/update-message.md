# Update Message with Discord

Updates a message in a Discord channel.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/channels/:channelId/messages/:messageId`
- **Base URL:** `https://discord.com/api/v10`
- **Official documentation:** [Update Message](https://docs.discord.com/developers/resources/message#edit-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | Channel identifier. |
| `messageId` | path | `string` | yes | Message identifier. |
| `content` | body | `string` | no | Updated message text content. |
| `embeds[]` | body | `array<object>` | no | Updated embeds array. |
| `components[]` | body | `array<object>` | no | Updated message components. |
| `attachments[]` | body | `array<object>` | no | Updated attachment objects. |
| `allowed_mentions` | body | `object` | no | Controls mention parsing for edited content. |
| `flags` | body | `number` | no | Message flags bitfield. |
