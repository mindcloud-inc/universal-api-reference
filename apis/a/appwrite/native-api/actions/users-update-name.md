# Update name with Appwrite

Updates the name in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/users/{userId}/name`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update name](https://appwrite.io/docs/references/cloud/server-rest/users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | User ID. |
| `name` | body | `string` | yes | User name. Max length: 128 chars. |
