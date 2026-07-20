# List user sessions with Appwrite

Retrieves a list of user sessions from your Appwrite project.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/{userId}/sessions`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [List user sessions](https://appwrite.io/docs/references/cloud/server-rest/users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | User ID. |
| `total` | query | `boolean` | no | When set to false, the total count returned will be 0 and will not be calculated. |
