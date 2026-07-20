# Update Account with Billforward

Updates an existing account in Billforward.

## Endpoint

- **Method:** `PUT`
- **Path:** `/accounts`
- **Base URL:** `https://app-sandbox.billforward.net/v1`
- **Official documentation:** [Update Account](https://app.billforward.net/#/api/method/accounts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The Billforward account ID to update. |
| `profile` | body | `object` | yes | Updated Billforward profile object. |
| `metadata` | body | `object` | no | Optional metadata object for the account update. |
