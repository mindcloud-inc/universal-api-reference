# Add a new user to Mumara with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/mumara/users`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Add a new user to Mumara](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | User's full name |
| `email` | body | `string` | yes | User's email address |
| `password` | body | `string` | yes | User's password |
| `password_confirmation` | body | `string` | no | Confirmation of the user's password |
| `package_id` | body | `number` | yes | Package/plan ID for the user |
| `timezone` | body | `string` | no | User's timezone |
| `login_ips` | body | `string` | no | Comma-separated allowed IP addresses |
| `hashed` | body | `boolean` | no | Whether password is already hashed |
| `response` | body | `number` | no | Response format type |
