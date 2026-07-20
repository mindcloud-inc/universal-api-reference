# Run Async SQL Query with Firebolt

Creates an asynchronous SQL query in Firebolt.

## Endpoint

- **Method:** `POST`
- **Path:** `https://:engineUrl`
- **Base URL:** `https://api.app.firebolt.io`
- **Official documentation:** [Run Async SQL Query](https://docs.firebolt.io/reference-api/using-async-queries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `engineUrl` | path | `string` | yes | Firebolt engine URL host or engine endpoint returned by Firebolt. |
| `database` | query | `string` | no | Database to target for user-engine async queries. |
| `engineName` | query | `string` | no | User engine name to target when submitting an async query to a user engine. |
| `sqlQuery` | body | `string` | yes | Async SQL statement to submit. |
