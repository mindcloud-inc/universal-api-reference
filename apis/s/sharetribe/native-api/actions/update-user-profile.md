# Update User Profile with Sharetribe

Updates an existing user profile in Sharetribe.

## Endpoint

- **Method:** `POST`
- **Path:** `users/update_profile`
- **Base URL:** `https://flex-integ-api.sharetribe.com/v1/integration_api`
- **Official documentation:** [Update User Profile](https://www.sharetribe.com/api-reference/integration.html#update-user-profile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The ID of the user that is being updated. |
| `firstName` | body | `string` | no | User's first name. |
| `lastName` | body | `string` | no | User's last name. |
| `displayName` | body | `string` | no | User's chosen display name. |
| `bio` | body | `string` | no | User's bio text. |
| `publicData` | body | `object` | no | User public extended data object. |
| `protectedData` | body | `object` | no | User protected extended data object. |
| `privateData` | body | `object` | no | User private extended data object. |
| `metadata` | body | `object` | no | User public metadata object. |
| `profileImageId` | body | `string` | no | Previously uploaded image ID to set as the user's profile image. |
