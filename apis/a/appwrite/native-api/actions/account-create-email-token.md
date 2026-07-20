# Create email token (OTP) with Appwrite

Creates a new email token OTP in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/account/tokens/email`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create email token (OTP)](https://appwrite.io/docs/references/cloud/server-rest/account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | body | `string` | yes | User ID. Choose a custom ID or generate a random ID with `ID.unique()`. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. If the email address has never been used, a new account is created using the provided userId. Otherwise, if the email address is already attached to an account, the user ID is ignored. |
| `email` | body | `string` | yes | User email. |
| `phrase` | body | `boolean` | no | Toggle for security phrase. If enabled, email will be send with a randomly generated phrase and the phrase will also be included in the response. Confirming phrases match increases the security of your authentication flow. |
