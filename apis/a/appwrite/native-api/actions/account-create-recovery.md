# Create password recovery with Appwrite

Creates a new password recovery in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/account/recovery`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create password recovery](https://appwrite.io/docs/references/cloud/server-rest/account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | User email. |
| `url` | body | `string` | yes | URL to redirect the user back to your app from the recovery email. Only URLs from hostnames in your project platform list are allowed. This requirement helps to prevent an [open redirect](https://cheatsheetseries.owasp.org/cheatsheets/Unvalidated_Redirects_and_Forwards_Cheat_Sheet.html) attack against your project API. |
