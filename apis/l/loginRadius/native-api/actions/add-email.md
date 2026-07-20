# Add Email with LoginRadius

Adds an email address to a LoginRadius account.

## Endpoint

- **Method:** `POST`
- **Path:** `/identity/v2/auth/email`
- **Base URL:** `https://api.loginradius.com`
- **Official documentation:** [Add Email](https://www.loginradius.com/docs/api/openapi/add-email/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accessToken` | body | `string` | yes | Access token for the logged-in user. |
| `email` | body | `string` | yes | Additional email address to add to the account. |
| `type` | body | `string` | no | Email type label for the new address. |
