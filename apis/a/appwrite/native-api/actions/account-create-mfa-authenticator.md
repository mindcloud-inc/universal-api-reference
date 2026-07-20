# Create authenticator with Appwrite

Creates a new authenticator in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/account/mfa/authenticators/{type}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create authenticator](https://appwrite.io/docs/references/cloud/server-rest/account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | path | `string` | yes | Type of authenticator. Must be `totp` |
