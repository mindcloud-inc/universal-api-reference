# Ban User with Stream

Bans a user in Stream.

## Endpoint

- **Method:** `POST`
- **Path:** `/moderation/ban`
- **Base URL:** `https://chat.stream-io-api.com`
- **Official documentation:** [Ban User](https://getstream.io/moderation/docs/api/flag-mute-ban/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target_user_id` | body | `string` | yes | User ID to ban. |
| `reason` | body | `string` | no | Reason for the ban. |
| `user_id` | body | `string` | yes | User ID performing the ban. |
