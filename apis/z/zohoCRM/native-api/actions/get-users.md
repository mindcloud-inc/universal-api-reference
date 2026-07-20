# Get Users with Zoho CRM

Retrieves user records from Zoho CRM.

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `{api_domain}/crm/v8`
- **Official documentation:** [Get Users](https://www.zoho.com/crm/developer/docs/api/v8/get-users.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `list` | no | User collection to return. Accepted values: `ActiveConfirmedAdmins`, `ActiveConfirmedUsers`, `ActiveUsers`, `AdminUsers`, `ConfirmedUsers`, `CurrentUser`, `CurrentUserAndAdmins`, `DeactiveUsers`, `DeletedUsers`, `NotConfirmedUsers`. |
