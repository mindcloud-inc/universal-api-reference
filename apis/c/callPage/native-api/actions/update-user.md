# Update User with CallPage

Updates an existing user in CallPage.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/update`
- **Base URL:** `https://core.callpage.io/api/v1/external`
- **Official documentation:** [Update User](https://callpage.github.io/documentation-rest/#update-user)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | body | `number` | yes |
| `name` | body | `string` | yes |
| `tel` | body | `string` | yes |
| `email` | body | `string` | no |
| `role` | body | `string` | no |
| `enabled` | body | `boolean` | yes |
