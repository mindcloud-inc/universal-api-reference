# Remove key permissions with Unkey

Removes permissions from an existing API key in Unkey.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/keys.removePermissions`
- **Base URL:** `https://api.unkey.com`
- **Official documentation:** [Remove key permissions](https://unkey.com/docs/api-reference/keys/remove-key-permissions)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `keyId` | body | `string` | yes |
| `permissions[]` | body | `array<string>` | yes |
