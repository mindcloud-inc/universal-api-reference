# Create User with Firebolt

Creates a new user in Firebolt.

## Endpoint

- **Method:** `POST`
- **Path:** `https://:engineHost`
- **Base URL:** `https://api.app.firebolt.io`
- **Official documentation:** [Create User](https://docs.firebolt.io/reference-sql/commands/access-control/create-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `engineHost` | path | `string` | yes | The Firebolt system engine host to send the SQL request to. |
| `userName` | body | `string` | yes | The Firebolt user name to create. |
| `serviceAccountName` | body | `string` | no | Optional Firebolt service account name to associate with the user. |
| `defaultDatabase` | body | `string` | no | Optional Firebolt default database for the user. |
| `defaultEngine` | body | `string` | no | Optional Firebolt default engine for the user. |
| `roleNames` | body | `string` | no | Optional comma-separated Firebolt role names to assign during user creation. |
