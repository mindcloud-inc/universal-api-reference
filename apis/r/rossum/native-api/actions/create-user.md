# Create User with Rossum

Creates a new user in Rossum.

## Endpoint

- **Method:** `POST`
- **Path:** `/users`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [Create User](https://rossum.app/api/docs/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | yes | First name of the user. |
| `last_name` | body | `string` | yes | Last name of the user. |
| `email` | body | `string` | yes | Email address for the new user. |
| `username` | body | `string` | yes | Rossum username for the new user, typically the same as the email. |
| `organization` | body | `string` | yes | Organization URL that owns the user. |
