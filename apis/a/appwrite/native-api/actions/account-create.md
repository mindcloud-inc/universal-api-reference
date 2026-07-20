# Create account with Appwrite

Creates a new account in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/account`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create account](https://appwrite.io/docs/references/cloud/server-rest/account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | body | `string` | yes | User ID. Choose a custom ID or generate a random ID with `ID.unique()`. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. |
| `email` | body | `string` | yes | User email. |
| `password` | body | `string` | yes | New user password. Must be between 8 and 256 chars. |
| `name` | body | `string` | no | User name. Max length: 128 chars. |
