# Retrieve Account with LoginRadius

Retrieves an account from LoginRadius by email, username, or phone.

## Endpoint

- **Method:** `GET`
- **Path:** `/identity/v2/manage/account`
- **Base URL:** `https://api.loginradius.com`
- **Official documentation:** [Retrieve Account](https://www.loginradius.com/docs/api/openapi/get-account-identity/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Email address to verify availability or retrieve associated Account. |
| `username` | query | `string` | no | Username to verify availability or retrieve associated Account. |
| `phone` | query | `string` | no | Phone number to verify availability or retrieve associated Account. |
| `q` | query | `string` | no | Query filter in key:value format. The key must be an indexed profile field. |
| `prevent_webhook` | query | `boolean` | no | When true, suppresses webhook events for this operation. |
