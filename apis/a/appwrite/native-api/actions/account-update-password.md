# Update password with Appwrite

Updates the password in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/account/password`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update password](https://appwrite.io/docs/references/cloud/server-rest/account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `password` | body | `string` | yes | New user password. Must be at least 8 chars. |
| `oldPassword` | body | `string` | no | Current user password. Must be at least 8 chars. |
