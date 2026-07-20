# Create Team User with Headless Testing

Creates a team user in Headless Testing.

## Endpoint

- **Method:** `POST`
- **Path:** `/team-management/users`
- **Base URL:** `https://api.testingbot.com/v1`
- **Official documentation:** [Create Team User](https://testingbot.com/support/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The team user's email address. |
| `first_name` | body | `string` | yes | The team user's first name. |
| `last_name` | body | `string` | yes | The team user's last name. |
| `password` | body | `string` | yes | The team user's password. |
