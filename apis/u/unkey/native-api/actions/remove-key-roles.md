# Remove key roles with Unkey

Removes roles from an existing API key in Unkey.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/keys.removeRoles`
- **Base URL:** `https://api.unkey.com`
- **Official documentation:** [Remove key roles](https://unkey.com/docs/api-reference/keys/remove-key-roles)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `keyId` | body | `string` | yes |
| `roles[]` | body | `array<string>` | yes |
