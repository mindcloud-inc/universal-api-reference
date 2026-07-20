# Find User with Range

Find a user by email or identity provider details.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/users/find`
- **Base URL:** `https://api.range.co`
- **Official documentation:** [Find User](https://www.range.co/docs/api#rpc-find-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `allow_inactive` | query | `boolean` | no | Whether to include deactivated users. |
| `allow_pending` | query | `boolean` | no | Whether to include pending users. |
| `email` | query | `string` | no | Plain text email address. |
| `email_hash` | query | `string` | no | Lowercase sha1 hash of the email. |
| `include_refs` | query | `boolean` | no | Whether to include the user object. |
| `provider` | query | `string` | no | Linked identity provider name. |
| `provider_id` | query | `string` | no | Provider-specific account ID. |
