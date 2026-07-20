# Delete User with Acronis

Deletes an existing user account from Acronis.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/2/users/{user_id}`
- **Base URL:** `{dataCenterUrl}`
- **Official documentation:** [Delete User](https://developer.acronis.com/doc/outbound/apis/api-library/account/users/deleting-user.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `string` | yes | User Id path parameter. |
