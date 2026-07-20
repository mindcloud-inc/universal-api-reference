# Create User with Discourse

Creates a new user in Discourse.

## Endpoint

- **Method:** `POST`
- **Path:** `/users.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Create User](https://docs.discourse.org/#tag/Users/operation/createUser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Full name. |
| `email` | body | `string` | yes | Email address. |
| `password` | body | `string` | yes | Initial password. |
| `username` | body | `string` | yes | Username. |
