# Send User Activation Email with Acronis

Sends a user activation email from Acronis.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/2/users/{user_id}/send-activation-email`
- **Base URL:** `{dataCenterUrl}`
- **Official documentation:** [Send User Activation Email](https://developer.acronis.com/doc/outbound/apis/api-library/account/users/activation/email.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `string` | yes | User Id path parameter. |
