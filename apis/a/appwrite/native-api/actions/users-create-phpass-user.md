# Create user with PHPass password with Appwrite

Creates a new user with PHPass password in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/phpass`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create user with PHPass password](https://appwrite.io/docs/references/cloud/server-rest/users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | body | `string` | yes | User ID. Choose a custom ID or pass the string `ID.unique()`to auto generate it. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. |
| `email` | body | `string` | yes | User email. |
| `password` | body | `string` | yes | User password hashed using PHPass. |
| `name` | body | `string` | no | User name. Max length: 128 chars. |
