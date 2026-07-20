# Delete Reaction with Stream

Deletes a reaction from a Stream message.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/messages/:id/reaction/:type`
- **Base URL:** `https://chat.stream-io-api.com`
- **Official documentation:** [Delete Reaction](https://getstream.io/chat/docs/javascript/send_reaction/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Message ID. |
| `type` | path | `string` | yes | Reaction type to delete. |
| `user_id` | query | `string` | yes | User ID whose reaction should be deleted. |
