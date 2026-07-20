# Update Chat with Pachca (Admin)

Updates an existing chat in the Pachca Admin API.

## Endpoint

- **Method:** `PUT`
- **Path:** `/chats/:id`
- **Base URL:** `https://api.pachca.com/api/shared/v1`
- **Official documentation:** [Update Chat](https://dev.pachca.com/api/chats/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Pachca chat ID. |
| `name` | body | `string` | no | — |
| `public` | body | `boolean` | no | — |
