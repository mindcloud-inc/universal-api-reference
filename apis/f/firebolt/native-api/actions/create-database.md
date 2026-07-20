# Create Database with Firebolt

Creates a new database in Firebolt.

## Endpoint

- **Method:** `POST`
- **Path:** `https://:engineUrl`
- **Base URL:** `https://api.app.firebolt.io`
- **Official documentation:** [Create Database](https://docs.firebolt.io/reference-sql/commands/data-definition/create-database)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `engineUrl` | path | `string` | yes | System engine host, for example 01kjtg5w4vwy72rfew4r8vg135.api.us-east-1.app.firebolt.io. |
| `databaseName` | body | `string` | yes | Name of the Firebolt database to create. |
| `description` | body | `string` | no | Optional database description, up to 64 characters. |
