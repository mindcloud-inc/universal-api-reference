# Stop Engine with Firebolt

Stops an engine in Firebolt.

## Endpoint

- **Method:** `POST`
- **Path:** `https://:engineHost`
- **Base URL:** `https://api.app.firebolt.io`
- **Official documentation:** [Stop Engine](https://docs.firebolt.io/reference-sql/commands/engines/stop-engine)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `engineHost` | path | `string` | yes | System engine host to execute the STOP ENGINE statement against. |
| `engineName` | body | `string` | yes | The running Firebolt engine to stop. |
| `terminate` | body | `boolean` | no | When true, stops the engine immediately without waiting for running queries to finish. |
