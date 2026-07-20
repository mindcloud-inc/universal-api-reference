# Update Account with Swell

## Endpoint

- **Method:** `PUT`
- **Path:** `/accounts/:id`
- **Base URL:** `https://api.swell.store`
- **Official documentation:** [Update Account](https://developers.swell.is/backend-api/accounts/update-an-account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Swell account ID. |
| `email` | body | `string` | no | The account email address. |
| `first_name` | body | `string` | no | The account first name. |
| `last_name` | body | `string` | no | The account last name. |
| `notes` | body | `string` | no | Internal notes for the account. |
