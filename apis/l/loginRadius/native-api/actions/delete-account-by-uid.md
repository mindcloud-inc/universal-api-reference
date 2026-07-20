# Delete Account by UID with LoginRadius

Deletes an existing account from LoginRadius by UID.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/identity/v2/manage/account/:uid`
- **Base URL:** `https://api.loginradius.com`
- **Official documentation:** [Delete Account by UID](https://www.loginradius.com/docs/api/openapi/delete-account-by-uid/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uid` | path | `string` | yes | UID of the account to delete. |
| `prevent_webhook` | query | `boolean` | no | Whether to suppress LoginRadius webhook processing for the delete operation. |
