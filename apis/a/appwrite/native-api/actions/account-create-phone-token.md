# Create phone token with Appwrite

Creates a new phone token in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/account/tokens/phone`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create phone token](https://appwrite.io/docs/references/cloud/server-rest/account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | body | `string` | yes | Unique Id. Choose a custom ID or generate a random ID with `ID.unique()`. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. If the phone number has never been used, a new account is created using the provided userId. Otherwise, if the phone number is already attached to an account, the user ID is ignored. |
| `phone` | body | `string` | yes | Phone number. Format this number with a leading '+' and a country code, e.g., +16175551212. |
