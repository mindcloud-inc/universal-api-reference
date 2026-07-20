# Unban User with Stream

Unbans a user in Stream.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/moderation/ban`
- **Base URL:** `https://chat.stream-io-api.com`
- **Official documentation:** [Unban User](https://getstream.io/moderation/docs/api/flag-mute-ban/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target_user_id` | query | `string` | yes | User ID to unban. |
