# Create Role with Firebolt

Creates a new role in Firebolt.

## Endpoint

- **Method:** `POST`
- **Path:** `https://:engineHost`
- **Base URL:** `https://api.app.firebolt.io`
- **Official documentation:** [Create Role](https://docs.firebolt.io/reference-sql/commands/access-control/create-role)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `engineHost` | path | `string` | yes | The Firebolt system engine host to send the SQL request to. |
| `roleName` | body | `string` | yes | The Firebolt role name to create. Firebolt role names should use valid identifier syntax. |
