# Upsert Users with Stream

Creates or updates users in Stream.

## Endpoint

- **Method:** `POST`
- **Path:** `/users`
- **Base URL:** `https://chat.stream-io-api.com`
- **Official documentation:** [Upsert Users](https://getstream.io/chat/docs/javascript/update_users/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `users` | body | `object` | yes | Map of user IDs to user objects to upsert. |
