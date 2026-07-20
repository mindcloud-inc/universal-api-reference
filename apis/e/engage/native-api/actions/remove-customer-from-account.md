# Remove Customer from Account with Engage

Removes a customer from an account in Engage.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/users/:uid/accounts/:aid`
- **Base URL:** `https://api.engage.so/v1`
- **Official documentation:** [Remove Customer from Account](https://docs.engage.so/en-us/a/62bbdd015bfea4dca4834042-users#remove-customer-from-an-account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uid` | path | `string` | yes | The customer user ID from your application. |
| `aid` | path | `string` | yes | The account user ID from your application. |
