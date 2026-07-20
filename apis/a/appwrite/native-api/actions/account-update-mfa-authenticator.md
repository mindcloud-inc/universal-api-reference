# Update authenticator (confirmation) with Appwrite

Completes MFA authenticator setup in Appwrite.

## Endpoint

- **Method:** `PUT`
- **Path:** `/account/mfa/authenticators/{type}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update authenticator (confirmation)](https://appwrite.io/docs/references/cloud/server-rest/account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | path | `string` | yes | Type of authenticator. |
| `otp` | body | `string` | yes | Valid verification token. |
