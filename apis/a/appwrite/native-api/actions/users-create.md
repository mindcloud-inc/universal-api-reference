# Create user with Appwrite

Creates a new user in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/users`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create user](https://appwrite.io/docs/references/cloud/server-rest/users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | body | `string` | yes | User ID. Choose a custom ID or generate a random ID with `ID.unique()`. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. |
| `email` | body | `string` | no | User email. |
| `phone` | body | `string` | no | Phone number. Format this number with a leading '+' and a country code, e.g., +16175551212. |
| `password` | body | `string` | no | Plain text user password. Must be at least 8 chars. |
| `name` | body | `string` | no | User name. Max length: 128 chars. |
