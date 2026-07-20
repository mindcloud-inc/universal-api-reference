# List Database Assets with PixieBrix

Retrieves assets from a PixieBrix database.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/databases/:database_pk/assets/`
- **Base URL:** `https://app.pixiebrix.com`
- **Official documentation:** [List Database Assets](https://docs.pixiebrix.com/developer-api/database-apis)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `database_pk` | path | `string` | yes | PixieBrix database identifier. |
