# Create user with bcrypt password with Appwrite

Creates a new user with bcrypt password in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/bcrypt`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create user with bcrypt password](https://appwrite.io/docs/references/cloud/server-rest/users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | body | `string` | yes | User ID. Choose a custom ID or generate a random ID with `ID.unique()`. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. |
| `email` | body | `string` | yes | User email. |
| `password` | body | `string` | yes | User password hashed using Bcrypt. |
| `name` | body | `string` | no | User name. Max length: 128 chars. |
