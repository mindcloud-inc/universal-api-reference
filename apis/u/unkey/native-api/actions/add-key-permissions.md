# Add key permissions with Unkey

Adds permissions to an existing API key in Unkey.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/keys.addPermissions`
- **Base URL:** `https://api.unkey.com`
- **Official documentation:** [Add key permissions](https://unkey.com/docs/api-reference/keys/add-key-permissions)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `keyId` | body | `string` | yes |
| `permissions[]` | body | `array<string>` | yes |
