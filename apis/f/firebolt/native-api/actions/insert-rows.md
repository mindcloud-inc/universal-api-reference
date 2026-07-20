# Insert Rows with Firebolt

Creates row inserts in Firebolt.

## Endpoint

- **Method:** `POST`
- **Path:** `https://:engineHost`
- **Base URL:** `https://api.app.firebolt.io`
- **Official documentation:** [Insert Rows](https://docs.firebolt.io/reference-sql/commands/data-management/insert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `engineHost` | path | `string` | yes | Firebolt user-engine host, for example account-1-mindcloud.api.us-east-1.app.firebolt.io. |
| `engineName` | query | `string` | no | Optional user engine name when routing through a shared user-engine host. |
| `database` | query | `string` | no | Optional database to target for the insert statement. |
| `tableName` | body | `string` | yes | Target table to insert rows into. |
| `columnList` | body | `string` | no | Optional comma-separated target columns for the insert statement. |
| `sourceClause` | body | `string` | yes | VALUES tuples or a SELECT query to insert. |
