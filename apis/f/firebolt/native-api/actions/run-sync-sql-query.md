# Run Sync SQL Query with Firebolt

Retrieves synchronous query results from Firebolt.

## Endpoint

- **Method:** `POST`
- **Path:** `https://:engineUrl`
- **Base URL:** `https://api.app.firebolt.io`
- **Official documentation:** [Run Sync SQL Query](https://docs.firebolt.io/reference-api/using-sync-queries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `engineUrl` | path | `string` | yes | The Firebolt engine host to send the SQL request to. |
| `database` | query | `string` | no | Optional database name. Required for user-engine queries and omitted for system-engine queries. |
| `engineName` | query | `string` | no | User engine name to target when querying a user engine. |
| `sqlQuery` | body | `string` | yes | A single Firebolt SQL statement to execute synchronously. |
