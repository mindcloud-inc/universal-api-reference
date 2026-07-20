# Reset Team User Credentials with Headless Testing

Resets a team user's credentials in Headless Testing.

## Endpoint

- **Method:** `PUT`
- **Path:** `/team-management/users/:id/reset-keys`
- **Base URL:** `https://api.testingbot.com/v1`
- **Official documentation:** [Reset Team User Credentials](https://testingbot.com/support/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Team user identifier from the path. |
