# Update phone with Appwrite

Updates the phone in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/users/{userId}/phone`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update phone](https://appwrite.io/docs/references/cloud/server-rest/users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | User ID. |
| `number` | body | `string` | yes | User phone number. |
