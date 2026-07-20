# Create user with Scrypt password with Appwrite

Creates a new user with Scrypt password in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/scrypt`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create user with Scrypt password](https://appwrite.io/docs/references/cloud/server-rest/users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | body | `string` | yes | User ID. Choose a custom ID or generate a random ID with `ID.unique()`. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. |
| `email` | body | `string` | yes | User email. |
| `password` | body | `string` | yes | User password hashed using Scrypt. |
| `passwordSalt` | body | `string` | yes | Optional salt used to hash password. |
| `passwordCpu` | body | `number` | yes | Optional CPU cost used to hash password. |
| `passwordMemory` | body | `number` | yes | Optional memory cost used to hash password. |
| `passwordParallel` | body | `number` | yes | Optional parallelization cost used to hash password. |
| `passwordLength` | body | `number` | yes | Optional hash length used to hash password. |
| `name` | body | `string` | no | User name. Max length: 128 chars. |
