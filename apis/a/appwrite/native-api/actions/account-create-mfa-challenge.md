# Create MFA challenge with Appwrite

Creates a new MFA challenge in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/account/mfa/challenges`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create MFA challenge](https://appwrite.io/docs/references/cloud/server-rest/account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `factor` | body | `string` | yes | Factor used for verification. Must be one of following: `email`, `phone`, `totp`, `recoveryCode`. |
