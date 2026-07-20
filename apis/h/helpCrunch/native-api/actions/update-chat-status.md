# Update Chat Status with HelpCrunch

Updates a chat's status in HelpCrunch.

## Endpoint

- **Method:** `PUT`
- **Path:** `/chats/status`
- **Base URL:** `https://api.helpcrunch.com/v1`
- **Official documentation:** [Update Chat Status](https://docs.helpcrunch.com/en/rest-api-v1/update-chat-status-v1)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | body | `number` | yes |
| `status` | body | `string` | yes |
