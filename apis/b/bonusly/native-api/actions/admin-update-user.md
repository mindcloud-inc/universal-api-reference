# Admin Update User with Bonusly

Updates an existing user in Bonusly.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/:id`
- **Base URL:** `https://bonus.ly/api/v1`
- **Official documentation:** [Admin Update User](https://docs.bonus.ly/reference/admin-update-a-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Updated email address. |
| `id` | path | `string` | yes | The Bonusly user ID. |
