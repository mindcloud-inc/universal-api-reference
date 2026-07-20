# Create User Management Session with Bridge

Creates a user management session in Bridge.

## Endpoint

- **Method:** `POST`
- **Path:** `/aggregation/user-management-sessions`
- **Base URL:** `https://api.bridgeapi.io/v3`
- **Official documentation:** [Create User Management Session](https://docs.bridgeapi.io/reference/createusermanagementsession)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userAccessToken` | body | `string` | yes | Bridge user access token returned by the Authorization token action. |
| `callback_url` | body | `string` | no | Optional callback URL for redirecting the user at the exit of the user management session |
| `context` | body | `string` | no | Optional context string to append to the callback URL when exiting the user management session. It can contain up to 100 alphanumeric characters, including the hyphen (-). |
| `account_types` | body | `string` | no | Minimum account types required. We suggest `payment` to ensure the best user experience |
| `user_email` | body | `string` | no | Mandatory, except in the case of temporary bank synchronization |
| `country_code` | body | `string` | no | On the displayed providers list, the country selector will default to the country parameter if provided. If you customize the highlighted banks on the dashboard, this parameter will be disabled. |
| `capabilities[]` | body | `array<string>` | no | Filter the provider capabilities you need. When multiple values are specified, they are combined using an `AND` operation |
| `allow_account_selection` | body | `boolean` | no | Allow or disallow the selection of the accounts |
