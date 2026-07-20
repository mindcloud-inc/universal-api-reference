# List Users with AppFollow

Retrieves users from AppFollow.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/account/users`
- **Base URL:** `https://api.appfollow.io`
- **Official documentation:** [List Users](https://docs.api.appfollow.io/reference/users_list_api_v2_account_users_get-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `number` | no | User ID filter. |
| `email` | query | `string` | no | Use this parameter to filter by email. |
