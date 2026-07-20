# Add Customer to Accounts with Engage

Adds a customer to one or more accounts in Engage.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/:uid/accounts`
- **Base URL:** `https://api.engage.so/v1`
- **Official documentation:** [Add Customer to Accounts](https://docs.engage.so/en-us/a/62bbdd015bfea4dca4834042-users#add-customer-to-accounts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accounts[]` | body | `array<object>` | yes | Array of account objects with id and optional role. |
| `uid` | path | `string` | yes | The customer user ID from your application. |
