# Create Role with Frontegg

Creates a new role in Frontegg.

## Endpoint

- **Method:** `POST`
- **Path:** `/identity/resources/roles/v1`
- **Base URL:** `https://api.frontegg.com`
- **Official documentation:** [Create Role](https://developers.frontegg.com/ciam/api/identity/roles)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | body | `string` | yes | Role key. |
| `name` | body | `string` | yes | Role name. |
| `description` | body | `string` | no | Role description. |
| `isDefault` | body | `boolean` | no | Assign this role by default to new users when no roles are specified. |
| `migrateRole` | body | `boolean` | no | Assign this role to all users when used with Is Default. |
| `firstUserRole` | body | `boolean` | no | Assign this role to the first user in new tenants. |
| `level` | body | `number` | yes | Role level; lower numbers are stronger roles. |
