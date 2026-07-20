# Get User Access Policies with Acronis

Retrieves access policies for a user in Acronis.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/2/users/{user_id}/access_policies`
- **Base URL:** `{dataCenterUrl}`
- **Official documentation:** [Get User Access Policies](https://developer.acronis.com/doc/outbound/apis/api-library/account/users/roles/check.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `string` | yes | User Id path parameter. |
