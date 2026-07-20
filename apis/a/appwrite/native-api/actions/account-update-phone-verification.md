# Update phone verification (confirmation) with Appwrite

Completes phone verification flow in Appwrite.

## Endpoint

- **Method:** `PUT`
- **Path:** `/account/verifications/phone`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update phone verification (confirmation)](https://appwrite.io/docs/references/cloud/server-rest/account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | body | `string` | yes | User ID. |
| `secret` | body | `string` | yes | Valid verification token. |
