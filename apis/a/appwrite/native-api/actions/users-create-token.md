# Create token with Appwrite

Creates a new token in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/{userId}/tokens`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create token](https://appwrite.io/docs/references/cloud/server-rest/users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | User ID. |
| `length` | body | `number` | no | Token length in characters. The default length is 6 characters |
| `expire` | body | `number` | no | Token expiration period in seconds. The default expiration is 15 minutes. |
