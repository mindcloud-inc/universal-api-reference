# Create User with Runrun.it

Creates a new user in Runrun.it.

## Endpoint

- **Method:** `POST`
- **Path:** `/users`
- **Base URL:** `https://runrun.it/api/v1.0`
- **Official documentation:** [Create User](https://runrun.it/api/documentation#users-create-a-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user.name` | body | `string` | yes | User's full name |
| `user.email` | body | `string` | yes | User's email |
| `make_my_partner` | body | `boolean` | no | Flag to make the new user a partner of the creating user |
| `make_everybody_mutual_partners` | body | `boolean` | no | Flag to make the new user a mutual partner of everybody in enterprise. If not set, defaults to enterprise's configuration |
