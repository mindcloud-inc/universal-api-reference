# Create User with StoryChief

Creates a new user in StoryChief.

## Endpoint

- **Method:** `POST`
- **Path:** `/users`
- **Base URL:** `https://api.storychief.io/1.0`
- **Official documentation:** [Create User](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-970e8e1a-45ab-4a8b-b9f4-ec5d1f409717)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | User email address. |
| `firstname` | body | `string` | no | User first name. |
| `lastname` | body | `string` | no | User last name. |
| `message` | body | `string` | no | Invitation message. |
| `role` | body | `string` | no | User role. |
