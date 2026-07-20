# Delete Account by Email with LoginRadius

Deletes an existing account from LoginRadius by email.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/identity/v2/manage/account`
- **Base URL:** `https://api.loginradius.com`
- **Official documentation:** [Delete Account by Email](https://www.loginradius.com/docs/api/openapi/delete-account-by-email/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | Email address of the account to delete. |
| `prevent_webhook` | query | `boolean` | no | Whether to suppress LoginRadius webhook processing for the delete operation. |
