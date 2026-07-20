# Reactivate User with Stream

Reactivates a user in Stream.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/:user_id/reactivate`
- **Base URL:** `https://chat.stream-io-api.com`
- **Official documentation:** [Reactivate User](https://getstream.io/chat/docs/javascript/update_users/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `string` | yes | User ID to reactivate. |
| `restore_messages` | body | `boolean` | no | Whether to restore messages when reactivating the user. |
