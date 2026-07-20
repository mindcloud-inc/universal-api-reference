# Set key permissions with Unkey

Sets permissions for an existing API key in Unkey.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/keys.setPermissions`
- **Base URL:** `https://api.unkey.com`
- **Official documentation:** [Set key permissions](https://unkey.com/docs/api-reference/keys/set-key-permissions)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `keyId` | body | `string` | yes |
| `permissions[]` | body | `array<string>` | yes |
