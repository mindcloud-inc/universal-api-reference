# Create user target with Appwrite

Creates a new user target in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/{userId}/targets`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create user target](https://appwrite.io/docs/references/cloud/server-rest/users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | User ID. |
| `targetId` | body | `string` | yes | Target ID. Choose a custom ID or generate a random ID with `ID.unique()`. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. |
| `providerType` | body | `string` | yes | The target provider type. Can be one of the following: `email`, `sms` or `push`. |
| `identifier` | body | `string` | yes | The target identifier (token, email, phone etc.) |
| `providerId` | body | `string` | no | Provider ID. Message will be sent to this target from the specified provider ID. If no provider ID is set the first setup provider will be used. |
| `name` | body | `string` | no | Target name. Max length: 128 chars. For example: My Awesome App Galaxy S23. |
