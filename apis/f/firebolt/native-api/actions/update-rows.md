# Update Rows with Firebolt

Updates existing rows in Firebolt.

## Endpoint

- **Method:** `POST`
- **Path:** `https://:engineHost`
- **Base URL:** `https://api.app.firebolt.io`
- **Official documentation:** [Update Rows](https://docs.firebolt.io/reference-sql/commands/data-management/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `engineHost` | path | `string` | yes | User engine host to execute the UPDATE statement against. |
| `engineName` | query | `string` | no | Optional engine name to send as the Firebolt engine query parameter. |
| `database` | query | `string` | no | Optional Firebolt database to execute the UPDATE statement in. |
| `tableName` | body | `string` | yes | The Firebolt table to update. |
| `tableAlias` | body | `string` | no | Optional alias for the target table. |
| `setClause` | body | `string` | yes | The UPDATE SET clause, for example status = 'archived', updated_at = CURRENT_TIMESTAMP. |
| `fromClause` | body | `string` | no | Optional FROM clause contents to join other tables into the UPDATE statement. |
| `whereClause` | body | `string` | no | Optional WHERE clause to restrict which rows are updated. |
| `settingsClause` | body | `string` | no | Optional WITH settings clause contents for query settings overrides. |
