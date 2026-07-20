# Update User with CompanyCam

Update an existing user in CompanyCam.

## Endpoint

- **Method:** `PUT`
- **Path:** `users/:id`
- **Base URL:** `https://api.companycam.com/v2/`
- **Official documentation:** [Update User](https://docs.companycam.com/reference/updateuser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | no | — |
| `last_name` | body | `string` | no | — |
| `email_address` | body | `string` | no | — |
| `phone_number` | body | `string` | no | — |
| `password` | body | `string` | no | — |
| `id` | path | `string` | yes | ID of the User |
