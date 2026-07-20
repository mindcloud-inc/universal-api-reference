# Firebolt Query Helper with Firebolt

Retrieves query results from Firebolt.

## Endpoint

- **Method:** `POST`
- **Path:** `https://:engineHost?engine=:engineName&database=:database&output_format=JSON_Compact`
- **Base URL:** `https://api.app.firebolt.io`
- **Official documentation:** [Firebolt Query Helper](https://docs.firebolt.io/guides/developing-with-firebolt/using-the-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `engineHost` | path | `string` | yes | Firebolt engine host without protocol. |
| `engineName` | path | `string` | yes | User engine name for the user-engine URL. |
| `database` | path | `string` | yes | Firebolt database name for the user-engine URL. |
| `sqlQuery` | body | `string` | yes | Raw SQL statement to execute. |
