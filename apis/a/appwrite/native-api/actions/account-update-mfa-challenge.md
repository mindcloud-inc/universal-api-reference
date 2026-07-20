# Update MFA challenge (confirmation) with Appwrite

Completes an MFA challenge in Appwrite.

## Endpoint

- **Method:** `PUT`
- **Path:** `/account/mfa/challenges`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update MFA challenge (confirmation)](https://appwrite.io/docs/references/cloud/server-rest/account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `challengeId` | body | `string` | yes | ID of the challenge. |
| `otp` | body | `string` | yes | Valid verification token. |
