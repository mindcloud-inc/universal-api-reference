# Update Account with Instantly

Updates an existing account in Instantly.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/accounts/:email`
- **Base URL:** `https://api.instantly.ai`
- **Official documentation:** [Update Account](https://developer.instantly.ai/api/v2/account/patchaccount)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | path | `string` | yes | Email of the account. |
| `first_name` | body | `string` | no | First name associated with the account. |
| `last_name` | body | `string` | no | Last name associated with the account. |
