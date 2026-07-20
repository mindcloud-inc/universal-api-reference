# Create user with SHA password with Appwrite

Creates a new user with SHA password in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/sha`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create user with SHA password](https://appwrite.io/docs/references/cloud/server-rest/users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | body | `string` | yes | User ID. Choose a custom ID or generate a random ID with `ID.unique()`. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. |
| `email` | body | `string` | yes | User email. |
| `password` | body | `string` | yes | User password hashed using SHA. |
| `passwordVersion` | body | `string` | no | Optional SHA version used to hash password. Allowed values are: 'sha1', 'sha224', 'sha256', 'sha384', 'sha512/224', 'sha512/256', 'sha512', 'sha3-224', 'sha3-256', 'sha3-384', 'sha3-512' |
| `name` | body | `string` | no | User name. Max length: 128 chars. |
