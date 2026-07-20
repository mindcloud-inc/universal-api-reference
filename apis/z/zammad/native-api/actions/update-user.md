# Update User with Zammad

Updates an existing user in Zammad.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/:id`
- **Base URL:** `{baseUrl}/api/v1`
- **Official documentation:** [Update User](https://docs.zammad.org/en/latest/api/user.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | User ID. |
| `phone` | body | `string` | yes | User phone number. |
