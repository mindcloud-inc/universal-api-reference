# Update phone with Appwrite

Updates the phone in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/account/phone`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update phone](https://appwrite.io/docs/references/cloud/server-rest/account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phone` | body | `string` | yes | Phone number. Format this number with a leading '+' and a country code, e.g., +16175551212. |
| `password` | body | `string` | yes | User password. Must be at least 8 chars. |
