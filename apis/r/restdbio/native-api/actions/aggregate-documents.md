# Aggregate Documents with Restdb.io

Retrieves aggregated document results from Restdb.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/:collection`
- **Base URL:** `https://mindcloudstage0-7934.restdb.io`
- **Official documentation:** [Aggregate Documents](https://restdb.io/media/restdb-cheat-sheet.pdf)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection` | path | `string` | yes | Collection name in the target Restdb.io database. |
| `h` | query | `string` | yes | JSON hint object for Restdb.io aggregation queries. |
