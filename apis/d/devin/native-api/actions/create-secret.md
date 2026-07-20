# Create Secret with Devin

Creates a new secret in Devin.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/organizations/:org_id/secrets`
- **Base URL:** `https://api.devin.ai`
- **Official documentation:** [Create Secret](https://docs.devin.ai/api-reference/v3/secrets/post-organizations-secrets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `is_sensitive` | body | `boolean` | no | Whether the secret is sensitive. |
| `key` | body | `string` | yes | Secret key/name. |
| `note` | body | `string` | no | Optional note for the secret. |
| `org_id` | path | `string` | yes | Devin organization ID. |
| `type` | body | `string` | yes | Secret type: cookie, key-value, or totp. |
| `value` | body | `string` | yes | Secret value. |
