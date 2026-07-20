# Create Account with Billforward

Creates a new account in Billforward.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts`
- **Base URL:** `https://app-sandbox.billforward.net/v1`
- **Official documentation:** [Create Account](https://app.billforward.net/#/api/method/accounts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profile` | body | `object` | yes | Billforward profile object for the new account. |
| `metadata` | body | `object` | no | Optional metadata object for the new account. |
