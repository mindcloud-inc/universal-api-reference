# Update Email with Discourse

Updates a Discourse user's email address.

## Endpoint

- **Method:** `PUT`
- **Path:** `/u/:username/preferences/email.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Update Email](https://docs.discourse.org/#tag/Users/operation/updateEmail)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | path | `string` | yes | Username. |
| `email` | body | `string` | yes | New email address. |
