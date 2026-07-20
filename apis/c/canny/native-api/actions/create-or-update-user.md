# Create or Update User with Canny

Creates or updates a user in Canny.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/users/create_or_update`
- **Base URL:** `https://canny.io/api`
- **Official documentation:** [Create or Update User](https://developers.canny.io/api-reference#create_or_update_user)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `alias` | body | `string` | no |
| `email` | body | `string` | no |
| `userID` | body | `string` | no |
| `id` | body | `string` | no |
| `name` | body | `string` | yes |
| `avatarURL` | body | `string` | no |
| `companies` | body | `list<object>` | no |
| `created` | body | `date` | no |
| `customFields` | body | `object` | no |
