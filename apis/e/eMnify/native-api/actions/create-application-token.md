# Create Application Token with EMnify

Creates a new application token in EMnify.

## Endpoint

- **Method:** `POST`
- **Path:** `/application_token`
- **Base URL:** `https://cdn.emnify.net/api/v1`
- **Official documentation:** [Create Application Token](https://docs.emnify.com/developers/api/application-tokens/application-token-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `auth_token` | body | `string` | yes | Auth token from Retrieve Authentication Token. |
| `description` | body | `string` | no | Description for the new application token. |
| `expiry_date` | body | `string` | no | Expiry date with optional time and time zone. |
| `ip` | body | `string` | no | Allowed IP address in CIDR notation. |
