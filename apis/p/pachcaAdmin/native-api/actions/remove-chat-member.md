# Remove Chat Member with Pachca (Admin)

Removes a chat member from the Pachca Admin API.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/chats/:id/members/:user_id`
- **Base URL:** `https://api.pachca.com/api/shared/v1`
- **Official documentation:** [Remove Chat Member](https://dev.pachca.com/api/members/remove)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Pachca chat ID. |
| `user_id` | path | `number` | yes | The Pachca user ID to remove from the chat. |
