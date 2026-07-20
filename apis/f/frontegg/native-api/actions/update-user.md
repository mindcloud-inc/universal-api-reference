# Update User with Frontegg

Updates an existing user in Frontegg.

## Endpoint

- **Method:** `PUT`
- **Path:** `/identity/resources/users/v1/:userId`
- **Base URL:** `https://api.frontegg.com`
- **Official documentation:** [Update User](https://developers.frontegg.com/ciam/api/identity/user-management)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | The user ID to update. |
| `name` | body | `string` | no | Updated user name. |
| `phoneNumber` | body | `string` | no | Updated user phone number in E.164 format. |
| `profilePictureUrl` | body | `string` | no | Updated profile picture URL. |
| `metadata` | body | `string` | no | Stringified JSON metadata. |
| `vendorMetadata` | body | `string` | no | Stringified JSON vendor metadata. |
| `mfaBypass` | body | `boolean` | no | Whether MFA should be bypassed for the user. |
| `externalId` | body | `string` | no | External identifier for the user. |
