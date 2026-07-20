# Delete View with Firebolt

Deletes an existing view from Firebolt.

## Endpoint

- **Method:** `POST`
- **Path:** `https://:engineHost`
- **Base URL:** `https://api.app.firebolt.io`
- **Official documentation:** [Delete View](https://docs.firebolt.io/reference-sql/commands/data-definition/drop-view)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `engineHost` | path | `string` | yes | User engine host to execute the DROP VIEW statement against. |
| `engineName` | query | `string` | no | Optional engine name to send as the Firebolt engine query parameter. |
| `database` | query | `string` | no | Optional Firebolt database to execute the DROP VIEW statement in. |
| `viewName` | body | `string` | yes | The Firebolt view to delete. |
| `ifExists` | body | `boolean` | no | When true, suppresses the error if the view does not exist. |
