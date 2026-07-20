# Update Message with Pachca (Admin)

Updates an existing message in the Pachca Admin API.

## Endpoint

- **Method:** `PUT`
- **Path:** `/messages/:id`
- **Base URL:** `https://api.pachca.com/api/shared/v1`
- **Official documentation:** [Update Message](https://dev.pachca.com/api/messages/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Pachca message ID. |
| `content` | body | `string` | yes | — |
