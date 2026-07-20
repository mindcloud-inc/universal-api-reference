# List Users with Bigin by Zoho CRM

Retrieves users from Bigin by Zoho CRM.

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `{api_domain}/bigin/v2`
- **Official documentation:** [List Users](https://www.bigin.com/developer/docs/apis/v2/get-users.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `list<string>` | no | The type of users to return. Accepted values: `ActiveConfirmedAdmins`, `ActiveConfirmedUsers`, `ActiveUsers`, `AdminUsers`, `AllUsers`, `ConfirmedUsers`, `CurrentUser`, `DeactiveUsers`, `DeletedUsers`, `NotConfirmedUsers`. |
