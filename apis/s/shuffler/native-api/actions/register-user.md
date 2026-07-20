# Register User with Shuffler

Creates a user in Shuffler.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/register`
- **Base URL:** `https://shuffler.io/api/v1`
- **Official documentation:** [Register User](https://shuffler.io/docs/API#register-a-new-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `password` | body | `string` | yes | User password. |
| `username` | body | `string` | yes | User email or username. |
