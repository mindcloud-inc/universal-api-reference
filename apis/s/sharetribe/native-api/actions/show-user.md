# Show User with Sharetribe

Retrieves a user from Sharetribe.

## Endpoint

- **Method:** `GET`
- **Path:** `users/show`
- **Base URL:** `https://flex-integ-api.sharetribe.com/v1/integration_api`
- **Official documentation:** [Show User](https://www.sharetribe.com/api-reference/integration.html#show-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | The user ID. Provide either user ID or email. |
| `email` | query | `string` | no | The user's email address. Provide either email or user ID. |
