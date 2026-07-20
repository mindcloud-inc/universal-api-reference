# List Users with noCRM.io

Retrieves users from noCRM.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `{baseUrl}/api/v2`
- **Official documentation:** [List Users](https://www.nocrm.io/api#list-all-the-users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Filter users by email. |
| `lastname` | query | `string` | no | Filter users by last name. |
| `firstname` | query | `string` | no | Filter users by first name. |
| `status` | query | `string` | no | User status filter. |
| `direction` | query | `string` | no | Sort direction for returned users. |
| `role` | query | `string` | no | User role filter. |
| `teams` | query | `list<string>` | no | Array of team IDs or names. Send multiple values as a string separated by `,`. |
