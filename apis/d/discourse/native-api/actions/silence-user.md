# Silence User with Discourse

Silences an existing user in Discourse.

## Endpoint

- **Method:** `PUT`
- **Path:** `/admin/users/:id/silence.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Silence User](https://docs.discourse.org/#tag/Users/operation/silenceUser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | User id. |
| `post_action` | body | `string` | no | Optional moderation action to take on the user's posts. Accepted values: `0`. |
| `silenced_till` | body | `string` | yes | Date/time until the user is silenced. |
| `reason` | body | `string` | yes | Silence reason. |
| `message` | body | `string` | no | Optional message sent with the silence. |
