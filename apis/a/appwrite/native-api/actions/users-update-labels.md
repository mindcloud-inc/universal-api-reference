# Update user labels with Appwrite

Updates the user labels in your Appwrite project.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/{userId}/labels`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update user labels](https://appwrite.io/docs/references/cloud/server-rest/users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `labels` | body | `string` | no | Array of user labels. Replaces the previous labels. Maximum of 1000 labels are allowed, each up to 36 alphanumeric characters long. |
| `userId` | path | `string` | yes | User ID. |
| `labels[]` | body | `array<string>` | yes | Array of user labels. Replaces the previous labels. Maximum of 1000 labels are allowed, each up to 36 alphanumeric characters long. |
