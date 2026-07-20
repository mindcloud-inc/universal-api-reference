# Update User with Shuffler

Updates an existing user in Shuffler.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/updateuser`
- **Base URL:** `https://shuffler.io/api/v1`
- **Official documentation:** [Update User](https://shuffler.io/docs/API#update-a-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `role` | body | `string` | yes | Updated role. |
| `user_id` | body | `string` | yes | User identifier. |
