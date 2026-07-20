# Create user JWT with Appwrite

Creates a new user JWT in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/{userId}/jwts`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create user JWT](https://appwrite.io/docs/references/cloud/server-rest/users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | User ID. |
| `sessionId` | body | `string` | no | Session ID. Use the string 'recent' to use the most recent session. Defaults to the most recent session. |
| `duration` | body | `number` | no | Time in seconds before JWT expires. Default duration is 900 seconds, and maximum is 3600 seconds. |
