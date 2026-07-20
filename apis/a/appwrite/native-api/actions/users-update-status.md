# Update user status with Appwrite

Updates the user status in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/users/{userId}/status`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update user status](https://appwrite.io/docs/references/cloud/server-rest/users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | User ID. |
| `status` | body | `boolean` | yes | User Status. To activate the user pass `true` and to block the user pass `false`. |
