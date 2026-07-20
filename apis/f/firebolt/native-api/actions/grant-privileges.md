# Grant Privileges with Firebolt

Creates privilege grants in Firebolt.

## Endpoint

- **Method:** `POST`
- **Path:** `https://:engineHost`
- **Base URL:** `https://api.app.firebolt.io`
- **Official documentation:** [Grant Privileges](https://docs.firebolt.io/reference-sql/commands/access-control/grant)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `engineHost` | path | `string` | yes | The Firebolt system engine host to send the SQL request to. |
| `privilege` | body | `string` | yes | The Firebolt privilege to grant, for example USAGE or SELECT. |
| `objectType` | body | `string` | yes | The Firebolt object type to grant against, for example DATABASE, SCHEMA, or TABLE. |
| `objectName` | body | `string` | yes | The Firebolt object name to grant against. |
| `containerObjectType` | body | `string` | no | Optional Firebolt parent object type used in the IN clause, for example DATABASE or SCHEMA. |
| `containerObjectName` | body | `string` | no | Optional Firebolt parent object name used in the IN clause. |
| `roleName` | body | `string` | yes | The Firebolt role name receiving the privilege. |
