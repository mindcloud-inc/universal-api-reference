# Create API Key with Resend

Creates a new API key in Resend.

## Endpoint

- **Method:** `POST`
- **Path:** `/api-keys`
- **Base URL:** `https://api.resend.com`
- **Official documentation:** [Create API Key](https://resend.com/docs/api-reference/api-keys/create-api-key)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | — |
| `permission` | body | `list<string>` | no | — |
| `domain_id` | body | `string` | no | Restrict an API key to send emails only from a specific domain. This is only used when the permission is set to sending_access. |
