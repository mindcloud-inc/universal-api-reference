# Update user preferences with Appwrite

Updates the user preferences in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/users/{userId}/prefs`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update user preferences](https://appwrite.io/docs/references/cloud/server-rest/users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | User ID. |
| `prefs` | body | `object` | yes | Prefs key-value JSON object. |
