# Create magic URL token with Appwrite

Creates a new magic URL token in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/account/tokens/magic-url`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create magic URL token](https://appwrite.io/docs/references/cloud/server-rest/account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | body | `string` | yes | Unique Id. Choose a custom ID or generate a random ID with `ID.unique()`. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. If the email address has never been used, a new account is created using the provided userId. Otherwise, if the email address is already attached to an account, the user ID is ignored. |
| `email` | body | `string` | yes | User email. |
| `url` | body | `string` | no | URL to redirect the user back to your app from the magic URL login. Only URLs from hostnames in your project platform list are allowed. This requirement helps to prevent an [open redirect](https://cheatsheetseries.owasp.org/cheatsheets/Unvalidated_Redirects_and_Forwards_Cheat_Sheet.html) attack against your project API. |
| `phrase` | body | `boolean` | no | Toggle for security phrase. If enabled, email will be send with a randomly generated phrase and the phrase will also be included in the response. Confirming phrases match increases the security of your authentication flow. |
