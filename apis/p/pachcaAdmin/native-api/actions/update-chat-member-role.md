# Update Chat Member Role with Pachca (Admin)

## Endpoint

- **Method:** `PUT`
- **Path:** `/chats/:id/members/:user_id`
- **Base URL:** `https://api.pachca.com/api/shared/v1`
- **Official documentation:** [Update Chat Member Role](https://dev.pachca.com/api/members/update-role)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Chat id. |
| `role` | body | `string` | yes | New chat role: admin, editor, or member. |
| `user_id` | path | `number` | yes | User id. |
