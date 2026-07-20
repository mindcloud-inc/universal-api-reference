# Update MFA with Appwrite

Updates the MFA in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/users/{userId}/mfa`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update MFA](https://appwrite.io/docs/references/cloud/server-rest/users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | User ID. |
| `mfa` | body | `boolean` | yes | Enable or disable MFA. |
