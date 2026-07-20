# Create Chat with Pachca (Admin)

Creates a new chat in the Pachca Admin API.

## Endpoint

- **Method:** `POST`
- **Path:** `/chats`
- **Base URL:** `https://api.pachca.com/api/shared/v1`
- **Official documentation:** [Create Chat](https://dev.pachca.com/api/chats/create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `member_ids[]` | body | `array<number>` | no |
| `group_tag_ids[]` | body | `array<number>` | no |
| `channel` | body | `boolean` | no |
| `public` | body | `boolean` | no |
