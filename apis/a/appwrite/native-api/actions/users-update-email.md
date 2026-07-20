# Update email with Appwrite

Updates the email in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/users/{userId}/email`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update email](https://appwrite.io/docs/references/cloud/server-rest/users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | User ID. |
| `email` | body | `string` | yes | User email. |
