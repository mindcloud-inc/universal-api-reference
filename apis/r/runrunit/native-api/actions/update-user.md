# Update User with Runrun.it

Updates an existing user in Runrun.it.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/:id`
- **Base URL:** `https://runrun.it/api/v1.0`
- **Official documentation:** [Update User](https://runrun.it/api/documentation#users-update-a-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Id path parameter. |
| `user.id` | body | `string` | yes | User's ID |
