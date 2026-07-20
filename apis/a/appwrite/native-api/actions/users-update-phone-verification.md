# Update phone verification with Appwrite

Updates the phone verification in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/users/{userId}/verification/phone`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update phone verification](https://appwrite.io/docs/references/cloud/server-rest/users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | User ID. |
| `phoneVerification` | body | `boolean` | yes | User phone verification status. |
