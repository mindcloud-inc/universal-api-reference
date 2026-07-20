# Update Username with Discourse

Updates the username for a Discourse user.

## Endpoint

- **Method:** `PUT`
- **Path:** `/u/:username/preferences/username.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Update Username](https://docs.discourse.org/#tag/Users/operation/updateUsername)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | path | `string` | yes | Username. |
| `new_username` | body | `string` | yes | Replacement username. |
