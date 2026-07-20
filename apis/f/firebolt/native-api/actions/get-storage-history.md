# Get Storage History with Firebolt

Retrieves storage history from Firebolt.

## Endpoint

- **Method:** `POST`
- **Path:** `https://:engineUrl`
- **Base URL:** `https://api.app.firebolt.io`
- **Official documentation:** [Get Storage History](https://docs.firebolt.io/reference-sql/information-schema/storage-history)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `engineUrl` | path | `string` | yes | System engine host, for example 01kjtg5w4vwy72rfew4r8vg135.api.us-east-1.app.firebolt.io. |
| `limit` | body | `number` | no | Maximum number of rows to return from information_schema.storage_history. |
