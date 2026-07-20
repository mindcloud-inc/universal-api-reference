# Retrieve Account by UID with LoginRadius

Retrieves an account from LoginRadius by UID.

## Endpoint

- **Method:** `GET`
- **Path:** `/identity/v2/manage/account/:uid`
- **Base URL:** `https://api.loginradius.com`
- **Official documentation:** [Retrieve Account by UID](https://www.loginradius.com/docs/api/openapi/get-account-identity-by-uid/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uid` | path | `string` | yes | The UID associated with the User. |
| `prevent_webhook` | query | `boolean` | no | When true, suppresses webhook events for this operation. |
