# Create Engine with Firebolt

Creates a new engine in Firebolt.

## Endpoint

- **Method:** `POST`
- **Path:** `https://:engineUrl`
- **Base URL:** `https://api.app.firebolt.io`
- **Official documentation:** [Create Engine](https://docs.firebolt.io/reference-sql/commands/engines/create-engine)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `engineUrl` | path | `string` | yes | System engine host, for example 01kjtg5w4vwy72rfew4r8vg135.api.us-east-1.app.firebolt.io. |
| `engineName` | body | `string` | yes | Name of the Firebolt engine to create. |
| `defaultDatabase` | body | `string` | no | Optional default database for the new engine. |
| `initiallyStopped` | body | `boolean` | no | When true, the new engine is created without starting immediately. |
| `autoStopMinutes` | body | `number` | no | Optional idle time in minutes before the engine auto-stops. |
| `engineType` | body | `string` | no | Optional engine type such as S or M. |
| `nodes` | body | `number` | no | Optional number of nodes per cluster. |
