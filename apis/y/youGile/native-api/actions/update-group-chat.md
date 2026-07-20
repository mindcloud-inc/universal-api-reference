# Update group chat with YouGile

Updates an existing group chat in YouGile.

## Endpoint

- **Method:** `PUT`
- **Path:** `/group-chats/:id`
- **Base URL:** `{companyDomain}/api-v2`
- **Official documentation:** [Update group chat](https://ru.yougile.com/api-v2#/operations/GroupChatController_update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The YouGile group chat ID. |
| `title` | body | `string` | no | The updated group chat title. |
| `users` | body | `object` | no | Updated map of chat users and notification settings. |
| `userRoleMap` | body | `object` | no | Updated map of user IDs to chat roles. |
| `roleConfigMap` | body | `object` | no | Updated role configuration map for the chat. |
| `deleted` | body | `boolean` | no | Mark the group chat as deleted. |
