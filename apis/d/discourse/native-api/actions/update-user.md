# Update User with Discourse

Updates an existing user in Discourse.

## Endpoint

- **Method:** `PUT`
- **Path:** `/u/:username.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Update User](https://docs.discourse.org/#tag/Users/operation/updateUser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Updated full name. |
| `username` | path | `string` | yes | Username. |
