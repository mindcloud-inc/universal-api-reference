# Add key roles with Unkey

Adds roles to an existing API key in Unkey.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/keys.addRoles`
- **Base URL:** `https://api.unkey.com`
- **Official documentation:** [Add key roles](https://unkey.com/docs/api-reference/keys/add-key-roles)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `keyId` | body | `string` | yes |
| `roles[]` | body | `array<string>` | yes |
