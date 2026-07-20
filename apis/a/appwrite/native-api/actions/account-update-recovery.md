# Update password recovery (confirmation) with Appwrite

Completes password recovery flow in Appwrite.

## Endpoint

- **Method:** `PUT`
- **Path:** `/account/recovery`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update password recovery (confirmation)](https://appwrite.io/docs/references/cloud/server-rest/account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | body | `string` | yes | User ID. |
| `secret` | body | `string` | yes | Valid reset token. |
| `password` | body | `string` | yes | New user password. Must be between 8 and 256 chars. |
