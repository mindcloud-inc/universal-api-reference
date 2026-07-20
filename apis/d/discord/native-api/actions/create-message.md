# Create Message with Discord

Creates a message in a Discord channel.

## Endpoint

- **Method:** `POST`
- **Path:** `/channels/:channelId/messages`
- **Base URL:** `https://discord.com/api/v10`
- **Official documentation:** [Create Message](https://docs.discord.com/developers/resources/message#create-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | Channel identifier. |
| `content` | body | `string` | no | Message text content. |
| `tts` | body | `boolean` | no | Whether this message should use text-to-speech. |
| `embeds[]` | body | `array<object>` | no | Rich embed objects for the message. |
| `allowed_mentions` | body | `object` | no | Controls which mentions are parsed. |
| `components[]` | body | `array<object>` | no | Message components such as buttons. |
| `sticker_ids[]` | body | `array<string>` | no | Sticker IDs to include with the message. |
| `attachments[]` | body | `array<object>` | no | Attachment objects for this message. |
| `message_reference` | body | `object` | no | Reference data for replies or forwards. |
| `flags` | body | `number` | no | Message flags bitfield. |
| `nonce` | body | `string` | no | Message nonce for validation. |
| `enforce_nonce` | body | `boolean` | no | Require nonce uniqueness for this send. |
| `poll` | body | `object` | no | Poll create request object. |
