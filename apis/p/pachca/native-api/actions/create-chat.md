# Create chat with Pachca

## Endpoint

- **Method:** `POST`
- **Path:** `/chats`
- **Base URL:** `https://api.pachca.com/api/shared/v1`
- **Official documentation:** [Create chat](https://dev.pachca.com/reference/chats-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chat` | body | `object` | yes | Chat parameters object. |
| `chat.name` | body | `string` | yes | Chat name. |
| `chat.member_ids[]` | body | `array<number>` | no | User IDs who will become chat members. Send multiple values as a array. |
| `chat.group_tag_ids[]` | body | `array<number>` | no | Group tag IDs to add as members. Send multiple values as a array. |
| `chat.channel` | body | `boolean` | no | Whether this chat is a channel. |
| `chat.public` | body | `boolean` | no | Whether this chat is publicly accessible. |
