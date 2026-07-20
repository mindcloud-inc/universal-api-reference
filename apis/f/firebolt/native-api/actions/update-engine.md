# Update Engine with Firebolt

Updates an existing engine in Firebolt.

## Endpoint

- **Method:** `POST`
- **Path:** `https://:engineHost`
- **Base URL:** `https://api.app.firebolt.io`
- **Official documentation:** [Update Engine](https://docs.firebolt.io/reference-sql/commands/engines/alter-engine)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `engineHost` | path | `string` | yes | System engine host to execute the ALTER ENGINE statement against. |
| `engineName` | body | `string` | yes | The Firebolt engine to alter. |
| `setClause` | body | `string` | yes | The ALTER ENGINE SET clause, for example AUTO_STOP = 15 or DEFAULT_DATABASE = my_database. |
