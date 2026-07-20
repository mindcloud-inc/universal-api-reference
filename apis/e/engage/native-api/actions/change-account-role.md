# Change Account Role with Engage

Updates a customer's role in an Engage account.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/:uid/accounts/:aid`
- **Base URL:** `https://api.engage.so/v1`
- **Official documentation:** [Change Account Role](https://docs.engage.so/en-us/a/62bbdd015bfea4dca4834042-users#change-account-role)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `role` | body | `string` | yes | The new role to set for the customer in the account. |
| `uid` | path | `string` | yes | The customer user ID from your application. |
| `aid` | path | `string` | yes | The account user ID from your application. |
