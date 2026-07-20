# Change Password with Discourse

Changes the password for a Discourse user.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/password-reset/:token.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Change Password](https://docs.discourse.org/#tag/Users/operation/changePassword)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `token` | path | `string` | yes | Password reset token. |
| `username` | body | `string` | yes | Username tied to the reset token. |
| `password` | body | `string` | yes | New password. |
