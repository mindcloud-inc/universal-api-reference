# Create user with Scrypt modified password with Appwrite

Creates a new user with Scrypt modified password in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/scrypt-modified`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create user with Scrypt modified password](https://appwrite.io/docs/references/cloud/server-rest/users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | body | `string` | yes | User ID. Choose a custom ID or generate a random ID with `ID.unique()`. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. |
| `email` | body | `string` | yes | User email. |
| `password` | body | `string` | yes | User password hashed using Scrypt Modified. |
| `passwordSalt` | body | `string` | yes | Salt used to hash password. |
| `passwordSaltSeparator` | body | `string` | yes | Salt separator used to hash password. |
| `passwordSignerKey` | body | `string` | yes | Signer key used to hash password. |
| `name` | body | `string` | no | User name. Max length: 128 chars. |
