# Update Avatar with Discourse

Updates the avatar for a Discourse user.

## Endpoint

- **Method:** `PUT`
- **Path:** `/u/:username/preferences/avatar/pick.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Update Avatar](https://docs.discourse.org/#tag/Users/operation/updateAvatar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | path | `string` | yes | Username. |
| `upload_id` | body | `number` | yes | Upload id to use for the avatar. |
| `type` | body | `string` | yes | Avatar source type. Accepted values: `0`, `1`, `2`, `3`. |
