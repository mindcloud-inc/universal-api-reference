# Update magic URL session with Appwrite

Updates the magic URL session in your Appwrite project.

## Endpoint

- **Method:** `PUT`
- **Path:** `/account/sessions/magic-url`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update magic URL session](https://appwrite.io/docs/references/cloud/server-rest/account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | body | `string` | yes | User ID. Choose a custom ID or generate a random ID with `ID.unique()`. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. |
| `secret` | body | `string` | yes | Valid verification token. |
