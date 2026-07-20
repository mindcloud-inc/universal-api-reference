# Create group chat with YouGile

Creates a new group chat in YouGile.

## Endpoint

- **Method:** `POST`
- **Path:** `/group-chats`
- **Base URL:** `{companyDomain}/api-v2`
- **Official documentation:** [Create group chat](https://ru.yougile.com/api-v2#/operations/GroupChatController_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | The group chat title. |
| `users` | body | `object` | yes | Map of chat users and notification settings. |
| `userRoleMap` | body | `object` | yes | Map of user IDs to chat roles. |
| `roleConfigMap` | body | `object` | yes | Role configuration map for the chat. |
