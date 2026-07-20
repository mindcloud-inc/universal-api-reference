# Alias with Vero

Aliases an existing user record in Vero.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v2/users/reidentify`
- **Base URL:** `https://api.getvero.com`
- **Official documentation:** [Alias](https://help.getvero.com/api-reference/users/alias)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The existing Vero user identifier to replace. |
| `new_id` | body | `string` | yes | The new Vero user identifier that should replace the existing one. |
