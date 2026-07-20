# Create User with CallPage

Creates a new user in CallPage.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/create`
- **Base URL:** `https://core.callpage.io/api/v1/external`
- **Official documentation:** [Create User](https://callpage.github.io/documentation-rest/#create-user)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `tel` | body | `string` | yes |
| `email` | body | `string` | no |
| `role` | body | `string` | no |
| `enabled` | body | `boolean` | yes |
