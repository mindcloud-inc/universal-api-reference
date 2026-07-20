# Vacuum Table with Firebolt

Updates table storage in Firebolt with VACUUM.

## Endpoint

- **Method:** `POST`
- **Path:** `https://:engineHost`
- **Base URL:** `https://api.app.firebolt.io`
- **Official documentation:** [Vacuum Table](https://docs.firebolt.io/reference-sql/commands/data-management/vacuum)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `engineHost` | path | `string` | yes | User engine host to execute the VACUUM statement against. |
| `engineName` | query | `string` | no | Optional engine name to send as the Firebolt engine query parameter. |
| `database` | query | `string` | no | Optional Firebolt database to execute the VACUUM statement in. |
| `tableName` | body | `string` | yes | The Firebolt table or aggregating index to vacuum. |
| `vacuumOptions` | body | `string` | no | Optional VACUUM options, for example INDEXES = NONE or MAX_CONCURRENCY = 1. |
