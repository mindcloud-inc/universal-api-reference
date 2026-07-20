# Create session with Appwrite

Creates a new session in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/{userId}/sessions`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create session](https://appwrite.io/docs/references/cloud/server-rest/users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | User ID. Choose a custom ID or generate a random ID with `ID.unique()`. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. |
