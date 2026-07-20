# Delete Engine with Firebolt

Deletes an existing engine from Firebolt.

## Endpoint

- **Method:** `POST`
- **Path:** `https://:engineHost`
- **Base URL:** `https://api.app.firebolt.io`
- **Official documentation:** [Delete Engine](https://docs.firebolt.io/reference-sql/commands/engines/drop-engine)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `engineHost` | path | `string` | yes | System engine host to execute the DROP ENGINE statement against. |
| `engineName` | body | `string` | yes | The Firebolt engine to delete. |
