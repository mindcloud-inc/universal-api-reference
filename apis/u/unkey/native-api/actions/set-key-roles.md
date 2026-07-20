# Set key roles with Unkey

Sets roles for an existing API key in Unkey.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/keys.setRoles`
- **Base URL:** `https://api.unkey.com`
- **Official documentation:** [Set key roles](https://unkey.com/docs/api-reference/keys/set-key-roles)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `keyId` | body | `string` | yes |
| `roles[]` | body | `array<string>` | yes |
