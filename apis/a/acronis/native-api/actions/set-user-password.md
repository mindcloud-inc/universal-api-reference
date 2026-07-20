# Set User Password with Acronis

Sets a user's password to activate the account in Acronis.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/2/users/{user_id}/password`
- **Base URL:** `{dataCenterUrl}`
- **Official documentation:** [Set User Password](https://developer.acronis.com/doc/outbound/apis/api-library/account/users/activation/password.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `string` | yes | User Id path parameter. |
