# Create Connect Session with Bridge

Creates a connect session in Bridge.

## Endpoint

- **Method:** `POST`
- **Path:** `/aggregation/connect-sessions`
- **Base URL:** `https://api.bridgeapi.io/v3`
- **Official documentation:** [Create Connect Session](https://docs.bridgeapi.io/reference/createconnectsession)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userAccessToken` | body | `string` | yes | Bridge user access token returned by the Authorization token action. |
| `user_email` | body | `string` | no | Mandatory, except in the case of temporary bank synchronization |
| `country_code` | body | `string` | no | On the displayed providers list, the country selector will default to the country parameter if provided. If you customize the highlighted banks on the dashboard, this parameter will be disabled. |
| `capabilities[]` | body | `array<string>` | no | Filter the provider capabilities you need. When multiple values are specified, they are combined using an `AND` operation |
| `allow_account_selection` | body | `boolean` | no | Allow or disallow the selection of the accounts |
| `max_selectable_accounts` | body | `number` | no | Max selectable accounts to be synchronized |
| `callback_url` | body | `string` | no | Optional callback URL for redirecting the user at the exit of the connect session |
| `context` | body | `string` | no | Optional context string to append to the callback URL when exiting the connect session. It can contain up to 100 alphanumeric characters, including the hyphen (-). |
| `account_types` | body | `string` | no | Minimum account types required. We suggest `payment` to ensure the best user experience |
| `provider_id` | body | `number` | no | If the parameter is set, the user will be directed straight to the relevant provider's authentication page (bypassing the providers list). Be sure to select a provider that supports at least the aggregation capability (see 'List providers') |
| `item_id` | body | `number` | no | The item for which you want to manage its connection state |
| `force_reauthentication` | body | `boolean` | no | Set this value to true if you want to renew the SCA immediately |
