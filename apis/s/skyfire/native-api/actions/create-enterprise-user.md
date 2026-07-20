# Create Enterprise User with Skyfire

Creates a new enterprise user in Skyfire.

## Endpoint

- **Method:** `POST`
- **Path:** `/organizations/users`
- **Base URL:** `https://api.skyfire.xyz/api/v1`
- **Official documentation:** [Create Enterprise User](https://docs.skyfire.xyz/reference/create-enterprise-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The email address of the new Enterprise User or Enterprise Admin User. |
| `role` | body | `string` | yes | The role of the new user. MEMBER for Enterprise User and ADMIN for Enterprise Admin User. |
