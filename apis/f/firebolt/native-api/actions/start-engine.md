# Start Engine with Firebolt

Starts an engine in Firebolt.

## Endpoint

- **Method:** `POST`
- **Path:** `https://:engineHost`
- **Base URL:** `https://api.app.firebolt.io`
- **Official documentation:** [Start Engine](https://docs.firebolt.io/reference-sql/commands/engines/start-engine)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `engineHost` | path | `string` | yes | System engine host to execute the START ENGINE statement against. |
| `engineName` | body | `string` | yes | The stopped Firebolt engine to start. |
