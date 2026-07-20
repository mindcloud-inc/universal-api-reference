# Delete User Data with Greip - Fraud Prevention

Deletes stored user data from Greip.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/account/users/delete`
- **Base URL:** `https://greipapi.com`
- **Official documentation:** [Delete User Data](https://docs.greip.io/api-reference/endpoint/account/users/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `value` | body | `string` | yes | The user identifier value whose related data should be deleted. |
