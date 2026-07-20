# Update user target with Appwrite

Updates the user target in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/users/{userId}/targets/{targetId}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update user target](https://appwrite.io/docs/references/cloud/server-rest/users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | User ID. |
| `targetId` | path | `string` | yes | Target ID. |
| `identifier` | body | `string` | no | The target identifier (token, email, phone etc.) |
| `providerId` | body | `string` | no | Provider ID. Message will be sent to this target from the specified provider ID. If no provider ID is set the first setup provider will be used. |
| `name` | body | `string` | no | Target name. Max length: 128 chars. For example: My Awesome App Galaxy S23. |
