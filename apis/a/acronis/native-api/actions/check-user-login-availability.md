# Check User Login Availability with Acronis

Checks whether a user login is available in Acronis.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/2/users/check_login`
- **Base URL:** `{dataCenterUrl}`
- **Official documentation:** [Check User Login Availability](https://developer.acronis.com/doc/outbound/apis/api-library/account/users/creating-user.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | query | `string` | yes | Username to check for availability. |
