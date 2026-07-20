# Delete Rows with Firebolt

Deletes existing rows from Firebolt.

## Endpoint

- **Method:** `POST`
- **Path:** `https://:engineHost`
- **Base URL:** `https://api.app.firebolt.io`
- **Official documentation:** [Delete Rows](https://docs.firebolt.io/reference-sql/commands/data-management/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `engineHost` | path | `string` | yes | User engine host to execute the DELETE statement against. |
| `engineName` | query | `string` | no | Optional engine name to send as the Firebolt engine query parameter. |
| `database` | query | `string` | no | Optional Firebolt database to execute the DELETE statement in. |
| `tableName` | body | `string` | yes | The Firebolt table to delete rows from. |
| `tableAlias` | body | `string` | no | Optional alias for the target table. |
| `usingClause` | body | `string` | no | Optional USING clause contents to join other tables into the DELETE statement. |
| `whereClause` | body | `string` | no | Optional WHERE clause to restrict which rows are deleted. |
| `settingsClause` | body | `string` | no | Optional WITH settings clause contents for query settings overrides. |
