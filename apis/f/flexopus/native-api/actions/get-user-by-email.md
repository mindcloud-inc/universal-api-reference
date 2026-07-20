# Get User by Email with Flexopus

Retrieves a Flexopus user by email address.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/by-email/:user_email`
- **Base URL:** `{tenantBaseUrl}/api/v1`
- **Official documentation:** [Get User by Email](https://flexopus.com/api/docs/#endpoints-GETapi-v1-users-by-email--user_email-)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_email` | path | `string` | yes | The email address of the user. |
