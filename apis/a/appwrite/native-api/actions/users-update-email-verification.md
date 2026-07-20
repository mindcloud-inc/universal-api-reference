# Update email verification with Appwrite

Updates the email verification in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/users/{userId}/verification`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update email verification](https://appwrite.io/docs/references/cloud/server-rest/users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | User ID. |
| `emailVerification` | body | `boolean` | yes | User email verification status. |
