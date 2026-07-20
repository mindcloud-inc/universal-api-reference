# Update email verification (confirmation) with Appwrite

Completes email verification flow in Appwrite.

## Endpoint

- **Method:** `PUT`
- **Path:** `/account/verifications/email`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update email verification (confirmation)](https://appwrite.io/docs/references/cloud/server-rest/account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | body | `string` | yes | User ID. |
| `secret` | body | `string` | yes | Valid verification token. |
