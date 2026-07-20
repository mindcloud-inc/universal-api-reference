# Update password with Appwrite

Updates the password in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/users/{userId}/password`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update password](https://appwrite.io/docs/references/cloud/server-rest/users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | User ID. |
| `password` | body | `string` | yes | New user password. Must be at least 8 chars. |
