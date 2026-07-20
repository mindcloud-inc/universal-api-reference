# Delete authenticator with Appwrite

Deletes the authenticator from your Appwrite project.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/users/{userId}/mfa/authenticators/{type}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Delete authenticator](https://appwrite.io/docs/references/cloud/server-rest/users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | User ID. |
| `type` | path | `string` | yes | Type of authenticator. |
